pipeline {
    agent any

    tools {
        maven 'Maven'
        jdk 'Java 8'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'mvn install'
            }
            post {
                success {
                    junit 'target/surefire-reports/**/*.xml'
                }
            }
        }
    }
}