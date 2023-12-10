pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Summan-Gul/TiCS.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying..'
                sshPublisher(
                    publishers: [
                        sshPublisherDesc(
                            configName: 'assignment4',
                            transfers: [sshTransfer(sourceFiles: '*/', remoteDirectory: '/home/ubuntu/myapp')]
                            
                        )
                    ]
                )
            }
        }
    }
}
