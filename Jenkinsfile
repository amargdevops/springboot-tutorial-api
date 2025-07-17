pipeline {
    agent any

   stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/amargdevops/springboot-tutorial-api.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        // Optional: Add Docker build stage later
    }

    post {
        success {
            echo 'Build & test completed successfully.'
        }
        failure {
            echo 'Something went wrong...'
        }
    }
}
