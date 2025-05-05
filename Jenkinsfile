pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    docker.build('my-image')
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    docker.image('my-image').inside {
                        sh 'npm test'
                    }
                }
            }
        }
    }
}
