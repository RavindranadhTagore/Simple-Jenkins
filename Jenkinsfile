pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/phanindra4568'
            }
        }

        stage('Build') {
            steps {
                script {
                    docker.build('my-app-image')
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests (placeholder)'
                // Ideally use a test framework here
            }
        }

        stage('Deploy') {
            steps {
                script {
                    docker.image('my-app-image').run('-d -p 5000:5000')
                }
            }
        }
    }
}