pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('python-flask-app', '.')
                }
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5001:5001 --name flask-app python-flask-app'
            }
        }
    }
}
