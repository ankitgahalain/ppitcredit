pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the code...'
                //Compile the code using Maven
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit tests...'
                //Run unit tests using Pytest
                echo 'Running integration tests...'
                //Run integration tests using Postman
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analyzing code...'
                //Analyse code using SonarQube
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing security scan...'
                //Run security scans using OWASP ZAP
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging environment...'
                //Deploy to a staging server like AWS EC2
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging...'
                //Run integration tests on Staging using Postman
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production environment...'
                //Deploy on production server like AWS EC2
            }
        }
    }
    post {
        success {
            emailext attachLog: true,
            body: 'Pipeline finished successfully. All stages completed successfully.',
            subject: 'Pipeline Status: Success',
            to: 'ankitgahalain@gmail.com'
        }
        failure {
            emailext attachLog: true,
            body: 'Pipeline failed. Check logs for details.',        
            subject: 'Pipeline Status: Failure',
            to: 'ankit.8243578@gmail.com'
        }
    }
}
