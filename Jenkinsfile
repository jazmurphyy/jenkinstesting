pipeline {
    agent any

    triggers {
        pollSCM('H/2 * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Task: Compile and package the application code.'
                echo 'Tool: Maven'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit tests and integration tests to check application functionality.'
                echo 'Tool: JUnit and Selenium'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Task: Analyse code quality, maintainability, bugs, and code smells.'
                echo 'Tool: SonarQube'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Task: Scan project dependencies and source code for known vulnerabilities.'
                echo 'Tool: OWASP Dependency-Check'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy the application to a staging server for testing.'
                echo 'Tool: AWS EC2'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Run integration tests in a production-like staging environment.'
                echo 'Tool: Postman/Newman'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Task: Deploy the tested application to the production server.'
                echo 'Tool: AWS EC2'
            }
        }
    }
}
