pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/NamanPatil08/Docker-ML.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t web-image-app .'
            }
        }
        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 8090:80 web-image-app'
            }
        }
    }
}