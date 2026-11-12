pipeline {
    agent any

    tools {
        maven 'Maven 3.9.6'
    }

    stages {
        stage('Build') {
            steps {
                echo 'compiling sysfoo application...'
                sh 'mvn compile'
            }
        }
        stage('Test') {
            steps {
                echo 'testing sysfoo application...'
                sh 'mvn clean test'
            }
        }
        stage('Package') {
            steps {
                echo 'packaging sysfoo application...'
                sh 'mvn package'
            }
        }
    }
    post {
        always {
            echo 'This pipeline is complete!'
        }
    }
}