pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/shivatechnology23/javatest.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean test'
            }
        }
    }
    post {
        always {
            junit 'target/surefire-reports/*.xml'
        }
    }
}
