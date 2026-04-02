pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-app .'
            }
        }

        stage('Deploy Container') {
            steps {
                sh 'docker run -d -p 8081:80 my-app'
            }
        }

    }
}
