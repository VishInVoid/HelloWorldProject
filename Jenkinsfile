pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning source code from GitHub...'
                git branch: 'main', url: 'https://github.com/VishInVoid/HelloWorldProject.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Java project...'
                sh 'javac HelloWorld.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Java program...'
                sh 'java HelloWorld'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check logs for details.'
        }
    }
}
