pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Build steps go here
                echo 'Building...'
                checkout scm
            }
        }

        stage('Test') {
            steps {
                // Test steps go here
                echo 'Testing...'
            }
        }

        stage('Deploy') {
            when {
                anyOf {
                    branch 'main'
                    branch 'develop'
                }
            }
            steps {
                // Deployment steps go here
                echo 'Deploying...'
            }
        }
    }
}
