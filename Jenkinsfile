pipeline {
    agent any
    tools { maven 'M3' }
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('Docker Image') {
            steps {
                script {
                    def dockerImage = docker.build("my-app:latest")
                }
            }
        }
    }
}