pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/diwakar237/sep17_milestone.git'
            }
        }
        stage('Build') {
            steps {
                bat '"C:\\Users\\lekha\\AppData\\Local\\Programs\\Python\\Python312\\python.exe" -m py_compile app.py'
                milestone(1)
                echo 'Build stage passed milestone 1'
            }
        }
        stage('Deploy') {
            steps {
                milestone(2)
                echo 'Deploying application...'
            }
        }
    }
}