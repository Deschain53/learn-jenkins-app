pipeline {
    agent any

    stages {
        stage('Build') {
            agend {
                docker {
                    image: 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm ci 
                    npm run build
                    ls -la
                '''
            }
        }
    }
}