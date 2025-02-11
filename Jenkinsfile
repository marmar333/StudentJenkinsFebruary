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
        stage('Run integration tests') {
            steps {
                bat 'docker build'
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
