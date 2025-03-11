pipeline {
    agent any 

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/PES2UG22CS676/PES2UG22CS676_Jenkins'
            }
        }

        stage('Build') {
            steps {
                sh 'g++ hello.cpp -o hello_exec'
            }
        }

        stage('Test') {
            steps {
                sh './hello_exec'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment successful!'
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline executed successfully!'
        }
        failure {
            echo '❌ Pipeline failed!'
        }
    }
}
