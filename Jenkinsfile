
pipeline {
    agent any

    tools {
        jdk 'jdk'
        maven 'maven3'
    }

    stages {

        stage('Git Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/mohitlohar1555-oss/CI-CD-project-with-K8S.git'
            }
        }

        stage('Code Compile') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Build Success') {
            steps {
                echo 'CI/CD Pipeline Executed Successfully!'
            }
        }
    }

    post {
        success {
            echo 'BUILD SUCCESS!'
        }

        failure {
            echo 'BUILD FAILED!'
        }
    }
}

