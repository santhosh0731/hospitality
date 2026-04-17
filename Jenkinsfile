pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Building project..."
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t hospitality-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5003:80 hospitality-app || true'
            }
        }
    }
}
