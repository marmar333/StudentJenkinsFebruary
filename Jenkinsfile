pipeline {
    agent any
    stages {
        stage('NPM Install') {
            steps {
                bat 'npm install'
            }
        }
       stage('Run npm audit tests') {
            steps {
                bat 'npm audit'
            }
        }
        stage('NPM Install') {
            steps {
                bat 'npm install'
                bat 'npm audit fix --force'  // Add this line to fix vulnerabilities
            }
        }
        stage('Run integration tests') {
            steps {
                bat 'npm run test'
            }
        }
        stage('Deploy to STAGING') {
            steps {
                echo 'Deploying to staging'
            }
        }
        stage('Deploy to PRODUCTION') {
            steps {
                echo 'Deploying to production'
            }
        }
    }
}
