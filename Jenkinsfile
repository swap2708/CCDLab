pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t jenkins-docker-demo .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker rm -f jenkins-demo-container || true'
                sh 'docker run -d --name jenkins-demo-container -p 5000:5000 jenkins-docker-demo'
            }
        }

        stage('Test Application') {
            steps {
                sh 'sleep 3'
                sh 'curl http://localhost:5000'
            }
        }
    }
}pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t jenkins-docker-demo .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker rm -f jenkins-demo-container || true'
                sh 'docker run -d --name jenkins-demo-container -p 5000:5000 jenkins-docker-demo'
            }
        }

        stage('Test Application') {
            steps {
                sh 'sleep 3'
                sh 'curl http://localhost:5000'
            }
        }
    }
}
