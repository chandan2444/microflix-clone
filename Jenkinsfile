pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                // This step automatically pulls your latest code from GitHub
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                // This runs the Dockerfile you created in Phase 1
                echo 'Building the Docker Image...'
                sh 'docker build -t netflix-clone:latest .'
            }
        }
    }
}
