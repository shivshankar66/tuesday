pipeline {
    agent any

    environment {
        IMAGE_NAME = 'shivam193/docker:90'
        DOCKER_CREDENTIALS = credentials('docker_credential')
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Docker Build & Push') {
            steps {
                bat """
                    echo %DOCKER_CREDENTIALS_PSW% | docker login -u %DOCKER_CREDENTIALS_USR% --password-stdin
                    docker build -t %IMAGE_NAME% .
                    docker push %IMAGE_NAME%
                """
            }
        }
    }
}