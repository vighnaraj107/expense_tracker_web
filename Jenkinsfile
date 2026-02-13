pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
                checkout scm
            }
        }

        stage('Deploy to Nginx') {
            steps {
                bat 'xcopy /E /Y expense C:\\nginx\\html\\expense\\'
            }
        }
    }
}
