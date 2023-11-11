pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }

        stage('Cloning Git Repo') {
            steps {
                script {
                    sh 'https://github.com/Viswesh934/2048-game.git'
                }
            }
        }

        stage('Installing Dependencies') {
            steps {
                script {
                    sh 'sudo apt install -y apache2'
                }
            }
        }

        stage('Moving Files') {
            steps {
                script {
                    sh 'sudo cp -r 2048-game/* /var/www/html'
                }
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }   
}
