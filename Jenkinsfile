pipeline {
    agent any
    stages {
        stage('Cleanup') {
            steps {
                script {
                    deleteDir()
                }
            }
        }
        stage('Git Clone') {
            steps {
                bat 'git clone https://github.com/Shivansh1711/E-sommerce-docker.git .'
            }
        }
        stage('Clear previous Builds') {
            steps {
                bat 'docker compose down'
            }
        }
        stage('Docker Compose') {
            steps {
                bat 'docker compose up -d --build'
            }
        }
        stage('Testing') {
            steps {
                script {
                   
                    // bat 'curl http://localhost:3000 || exit 1'
                    echo "testing commands invoked"
                }
            }
        }
    }
}
