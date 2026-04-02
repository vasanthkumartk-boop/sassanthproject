pipeline {
    agent any
            stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-app .'
            }
        }

        stage('Deploy Container') {
            steps {
                sh '''
                docker stop my-app || true
                docker rm my-app || true
                docker run -d -p 80:80 --name my-app my-app
                '''
            }
        }
    }
}
