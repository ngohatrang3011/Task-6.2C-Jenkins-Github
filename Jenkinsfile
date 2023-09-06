pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the code...'
                // Use a build automation tool like Maven to build your code
                // Example: sh 'mvn clean package'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests...'
                // Use test automation tools for unit and integration tests
                // Example: sh 'npm test'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Running code analysis...'
                // Integrate a code analysis tool (e.g., SonarQube)
                // Example: sh 'sonar-scanner'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing a security scan...'
                // Perform a security scan using a security scanning tool
                // Example: sh 'safety check'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging environment...'
                // Deploy to your staging environment (e.g., AWS EC2)
                // Example: sh 'ansible-playbook deploy-staging.yml'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on the staging environment...'
                // Run integration tests on the staging environment
                // Example: sh 'cypress run --env staging'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production environment...'
                // Deploy to your production environment (e.g., AWS EC2)
                // Example: sh 'ansible-playbook deploy-production.yml'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline succeeded!'
            emailext subject: 'Pipeline Success',
                body: 'The pipeline succeeded. See attached logs.',
                to: 'cielo30112000@gmail.com'
        }
        failure {
            echo 'Pipeline failed!'
            emailext subject: 'Pipeline Failure',
                body: 'The pipeline failed. See attached logs.',
                to: 'cielo30112000@gmail.com'
        }
    }
}
