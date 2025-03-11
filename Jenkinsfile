pipeline {
    agent any

    environment {
        // Set environment variables if needed
        NODE_ENV = 'production'
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from GitHub
                git branch: 'main', url: 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                // Install Node.js and dependencies
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                // Build the React app
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                // Run tests (if any)
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the app (e.g., to a server or S3 bucket)
                sh 'echo "Deploying the app..."'
                // Add deployment commands here
            }
        }
    }

    post {
        success {
            // Actions to perform on success
            echo 'Pipeline succeeded!'
        }
        failure {
            // Actions to perform on failure
            echo 'Pipeline failed!'
        }
    }
}
