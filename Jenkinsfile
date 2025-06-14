pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('python-flask-app', './app')
                }
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 --name flask-app python-flask-app'
            }
        }
    }
}
