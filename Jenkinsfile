pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Specify the Git repository URL and the branch to checkout
                    git branch: 'main', url: 'https://github.com/ally0/github'
                }
            }
        }
    }
}
