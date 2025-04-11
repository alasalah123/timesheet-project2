pipeline {
    agent any
    environment {
        NEXUS_CREDENTIALS = credentials('nexus') // Jenkins credentials ID = 'nexus'
    }
    stages {
        stage('GIT') {
            steps {
                git 'https://github.com/alasalah123/timesheet-project2.git'
            }
        }
        stage('COMPILATION') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('DEPLOYMENT') {
            steps {
                sh 'mvn deploy'
            }
        }
    }
}

