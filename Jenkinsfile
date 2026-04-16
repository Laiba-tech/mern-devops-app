pipeline {
    agent any

    stages {

        stage('Build Containers') {
            steps {
                bat "docker-compose down || exit 0"
                bat "docker-compose up --build -d"
            }
        }

        stage('Verify') {
            steps {
                bat "docker ps"
            }
        }
    }
}
