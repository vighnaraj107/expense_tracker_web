pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                dir('expense') {
                    bat 'npm install'
                }
            }
        }

        stage('Build Project') {
            steps {
                dir('expense') {
                    bat 'npm run build'
                }
            }
        }

        stage('Deploy to Nginx') {
            steps {
                bat 'xcopy /E /Y expense\\dist\\* C:\\nginx\\html\\'
            }
        }
    }
}
