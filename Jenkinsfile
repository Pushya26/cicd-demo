pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Pushya26/cicd-demo.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t cicd-demo:latest .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8081:80 --name cicd-demo-app cicd-demo:latest'
            }
        }
    }
}
