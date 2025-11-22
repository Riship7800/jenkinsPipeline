pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/Riship7800/jenkinsPipeline'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("myapp:latest")
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    docker.image("myapp:latest").run("-d -p 8080:8080")
                }
            }
        }
    }
}
