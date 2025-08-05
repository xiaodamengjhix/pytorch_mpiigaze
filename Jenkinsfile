pipeline {
    agent {
        docker {
            image 'python:3.8'
        }
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Test') {
            steps {
                sh 'pip install -r requirements.txt && pytest'
            }
        }
    }
}