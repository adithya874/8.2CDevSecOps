pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }
        stage('Code Formatting') {
            steps {
                echo 'Checking formatting...'
                sh 'npm run format'
            }
        }
        stage('Static Analysis') {
            steps {
                echo 'Running lint...'
                sh 'npm run lint'
            }
        }
        stage('Unit Tests') {
            steps {
                echo 'Running tests...'
                sh 'npm test'
            }
        }
        stage('Build') {
            steps {
                echo 'Building app...'
                sh 'npm run build'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'echo Deploying to server...'
            }
        }
    }
}
