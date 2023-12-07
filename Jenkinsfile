pipeline {
    agent any
    
    tools {
        nodejs "nodejs"
    }
    
    stages {
        stage('Install Packages') {
            steps {
                script {
                    sh 'npm install'
                }
            }
        }

        stage('Run the App') {
            steps {
                script {
                    sh 'npm start &'
                    sleep 5
                }
            }
        }

        stage('Test the app') {
            steps {
                script {
                    sh 'curl http://localhost:3000/health'
                }
            }
        }
    }
}
