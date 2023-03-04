pipeline {
    agent any
    tools { 'M3' }
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