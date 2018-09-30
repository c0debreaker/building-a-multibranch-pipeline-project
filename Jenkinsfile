pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3500:3500 -p 5500:5500' 
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}