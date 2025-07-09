pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git credentialsId: 'github-https', url: 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Install') {
            steps {
                sh 'echo "Install dependencies"'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Run build step"'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "Run tests"'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploy app"'
            }
        }
    }
}
