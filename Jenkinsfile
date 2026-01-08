pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                echo 'Pulling code from GitHub'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project'
                dir('.'){
                    bat 'echo Build completed'
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
                bat 'if exist test.txt (echo Tests Passed) else (exit 1)'
            }
        }

        stage('Package') {
            steps {
                echo 'Packaging application'
                bat 'mkdir output'
                bat 'copy index.html output\\index.html'
            }
        }

        stage('Ready for Deploy') {
            steps {
                echo 'Application is ready for deployment'
            }
        }
    }
}

