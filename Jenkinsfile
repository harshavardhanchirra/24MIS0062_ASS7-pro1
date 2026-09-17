pipeline {
    agent any

    parameters {
        choice(name: 'ENVIRONMENT', choices: ['dev', 'staging', 'prod'], description: 'Select the deployment environment')
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/harshavardhanchirra/24MIS0062_ASS7-pro1.git'
            }
        }

        stage('Build') {
            steps {
                bat 'javac StudentManagement.java'
            }
        }

        stage('Show Parameter') {
            steps {
                echo "Selected environment: ${params.ENVIRONMENT}"
                echo "Student Management System built for ${params.ENVIRONMENT}"
            }
        }
    }
}
