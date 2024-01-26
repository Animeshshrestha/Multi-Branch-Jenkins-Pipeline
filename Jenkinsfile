pipeline {
    agent any

    stages {

        stage('Code Checkout') {
            steps {
                checkout([
                    $class: 'GitSCM', 
                    branches: [[name: '*/main']], 
                    userRemoteConfigs: [[url: 'https://github.com/Animeshshrestha/Multi-Branch-Jenkins-Pipeline.git']]
                ])
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
