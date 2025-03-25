pipeline {
    agent any

    tools {
        nodejs 'NodeJS'  // This should match the name set in Step 3
    }

    stages {
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
    }
}
