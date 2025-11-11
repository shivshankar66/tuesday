pipeline {
    agent any

    environment {
        IMAGE_NAME = 'shivam193/docker:90'
        DOCKER_CREDENTIALS = credentials('docker_credential') // Jenkins credentials ID
        KUBECONFIG = 'D:\\Users\\DELL\\Desktop\\JENKINSFOLDER\\.kube\\config'
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

        stage('Deploy to Kubernetes') {
            steps {
                bat 'kubectl apply -f Depservice.yml'
            }
        }
    }
}