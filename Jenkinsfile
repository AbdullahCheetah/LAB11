pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                sh 'Checkout passed'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'echo docker build -t $DOCKER_IMAGE .'
            }
        }
        stage('Run Docker Image') {
            steps {
                sh 'echo docker run -d -p 80:80 $DOCKER_IMAGE'
            }
        }
        stage('Push Docker Image') {
            steps {
                sh 'echo docker push abdullah/lab11:latest'  
            }
        }
    }
    
}
