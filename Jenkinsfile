pipeline {
    agent any

    tools {
        maven 'Maven1'
    }

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying using Ansible'
            }
        }
    }
}
