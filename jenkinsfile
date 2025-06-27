pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/Athul-mj/flask-jenkins-docker-demo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('flask-jenkins-app')
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    docker.image('flask-jenkins-app').run('-p 5000:5000')
                }
            }
        }
    }
}
