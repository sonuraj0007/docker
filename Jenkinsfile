pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-nginx-website:latest .'
            }
        }

        stage('Verify Image') {
            steps {
                sh 'docker images my-nginx-website:latest'
            }
        }
    }
}