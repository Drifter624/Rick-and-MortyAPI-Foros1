pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Drifter624/Rick-and-MortyAPI-Foros1.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('rick-morty-api-docker').inside {
                        echo 'Docker container is up and running!'
                    }
                }
            }
        }
    }
    post {
        always {
            echo 'Pipeline completed.'
        }
    }
}
