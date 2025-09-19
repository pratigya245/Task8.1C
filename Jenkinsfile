pipeline {
    agent any

    triggers {
        // Poll SCM every 5 minutes 
        pollSCM('H/5 * * * *') 
    }

    stages {
        stage('Build') {
            steps {
                echo 'Stage 1: Build - Compile and package the application code.'
                echo 'Tool: Maven or Gradle' 
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Stage 2: Unit and Integration Tests - Run unit tests and integration tests.'
                echo 'Tools: JUnit (for unit tests), TestNG (for integration tests)' 
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Stage 3: Code Analysis - Analyze code for quality and standards.'
                echo 'Tool: SonarQube'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Stage 4: Security Scan - Identify security vulnerabilities in the code.'
                echo 'Tool: OWASP Dependency-Check or Snyk'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Stage 5: Deploy to Staging - Deploy application to staging environment.'
                echo 'Tool: AWS EC2 (with Ansible or Jenkins deploy plugin)'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Integration Tests on Staging - Run tests in staging environment.'
                echo 'Tools: Selenium or Postman'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Stage 7: Deploy to Production - Deploy application to production environment.'
                echo 'Tool: AWS EC2 (with Ansible, Terraform, or Jenkins deploy plugin)'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Please check the logs.'
        }
    }
}
