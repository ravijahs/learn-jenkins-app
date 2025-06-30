pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    ls -al
                    node --version
                    npm --version
                    pm ci
                    npm run build
                    ls -al
                '''
            }
        }
        stage('Test') {
            steps {
                ehco 'Step Stage'
            }
        }
    }
}