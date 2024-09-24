pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout from GitHub
                git branch: 'main', url: 'https://github.com/ally0/github'
            }
        }

        stage('Build') {
            steps {
                // Add your build commands here
                echo 'Building the project...'
                // Example: sh 'make me'
            }
        }

        stage('Test') {
            steps {
                // Add your test commands here
                echo 'Running tests...'
                // Example: sh 'make me'
            }
        }

        stage('Check Changes') {
            steps {
                script {
                    def changes = sh(script: 'git diff --name-only HEAD^ HEAD', returnStdout: true).trim()
                    if (changes) {
                        echo "Changes detected: ${changes}"
                    } else {
                        echo "No changes detected."
                    }
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}
