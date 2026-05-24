pipeline {
    agent any
 
    triggers {
        githubPush()
    }
 
    stages {
 
        stage('Checkout') {
            steps {
                git branch: 'master',
                url: 'https://github.com/1907CharanReddy/pipeline1.git'
            }
        }
 
        stage('Build') {
            steps {
                sh 'echo "Building Python project..."'
            }
        }
 
        stage('Test') {
            steps {
                sh 'python3 app.py'
            }
        }
 
    }
 
    post {
        success {
            echo 'Build succeeded!'
        }
 
        failure {
            echo 'Build failed!'
        }
    }
}
