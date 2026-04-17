pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/santhosh0731/hospitality.git'
            }
        }

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
                sh 'docker run -d -p 5002:80 hospitality-app || true'
            }
        }
    }
}
