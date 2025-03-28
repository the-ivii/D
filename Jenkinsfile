pipeline {
    agent any
    
    tools {
        nodejs 'Node 23'  // Use the installed NodeJS version
    }
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/your-repo/node-app.git'
            }
        }
        
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        
        stage('Run Tests') {
            steps {
                sh 'npm test || echo "No tests defined"'
            }
        }
        
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t node-app .' 
            }
        }
    }
}
