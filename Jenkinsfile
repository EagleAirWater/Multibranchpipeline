pipeline {

    environment {
        // Retrieve the current branch name as an environment variable
        BRANCH_NAME = "${env.BRANCH_NAME}"
    }

    agent any

    stages {
        stage('Checkout') {
            git branch: '${env.BRANCH_NAME}'
        }

        stage('Print Branch Message') {
            // Conditional statement to print branch-specific messages
            script {
                if (env.BRANCH_NAME == 'master') {
                    echo 'Hello on master'
                } else if (env.BRANCH_NAME == 'release') {
                    echo 'Hello on release'
                } else {
                    echo "Hello on branch: ${env.BRANCH_NAME}" // Generic message for other branches
                }
            }
        }

        // Additional stages for potential build and deployment steps (replace with your actual logic)
        // ... (e.g., build, test, deploy)
    }
}

