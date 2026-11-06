
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Fetching project from GitHub'
            }
        }

        stage('Java Build') {
            steps {
                bat 'javac prime.java'
            }
        }

        stage('Python Check') {
            steps {
                bat 'python --version'
                bat 'python -m py_compile Flask_Login/app.py'
            }
        }

        stage('Build Complete') {
            steps {
                echo 'All build stages completed successfully!'
            }
        }
    }
}
