pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'git@github.com:ferozqureshifk786-design/devops-lab.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-lab:v1 ./app'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 devops-lab:v1 || true'
            }
        }

    }
}
