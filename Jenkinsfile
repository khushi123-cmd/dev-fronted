pipeline {
    agent any

    stages {

        stage('Check Workspace') {
            steps {
                bat 'cd'
                bat 'dir'
            }
        }

        stage('Build & Deploy with Docker Compose') {
            steps {
                bat '''
                docker compose down
                docker compose up -d --build
                '''
            }
        }
    }
}
