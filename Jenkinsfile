pipeline {
    agent any

    tools {
        maven 'Maven1'
    }

    stages {

        stage('Build') {
            steps {
                dir('myapp') {
                    bat 'mvn clean install'
                }
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'myapp/target/*.jar'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying using Ansible'
            }
        }

    }
}
