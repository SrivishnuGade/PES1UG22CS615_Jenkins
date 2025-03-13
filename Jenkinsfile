pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/SrivishnuGade/PES1UG22CS615_Jenkins.git'
            }
        }
        stage('Build application') {
            steps {
                sh 'g++ -o PES1UG22CS615-1 main/hello.cpp'  
            }
        }
        stage('Test application') {
            steps {
                sh './PES1UG22615-1'  
            }
        }
        stage('Deploy application') {
            steps {
                echo 'Deploying application...'  
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!' 
        }
        success {
            echo 'Pipeline executed successfully!'  
        }
    }
}