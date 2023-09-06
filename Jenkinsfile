pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the code using Maven...'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests with JUnit ...'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Running code analysis using SonarQube...'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing a security scan using OWASP ZAP...'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging environment AWS EC2...'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on the staging environment...'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production environment with AWS EC2...''
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline succeeded!'
            emailext (attachLog: true, body: 'The pipeline succeeded. See attached logs.', subject: 'Pipeline Success', to: 'cielo30112000@gmail.com')
        }
        failure {
            echo 'Pipeline failed!'
            emailext (attachLog: true, body: 'The pipeline failed. See attached logs.', subject: 'Pipeline Failure', to: 'cielo30112000@gmail.com')
        }
    }
}
