pipeline {
    agent any

    environment {
        NODEJS_HOME = tool 'NodeJS' // Ensure NodeJS is configured in Jenkins
        PATH = "${NODEJS_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Pulkit-Kumar-0/React-app.git' 
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build React App') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test -- --watchAll=false'
            }
        }

        stage('Deploy (Optional)') {
            steps {
                echo 'Deploying the application...'
                // Add deployment steps here
            }
        }
    }
}
