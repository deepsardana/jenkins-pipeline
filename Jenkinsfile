pipeline {
    agent any

    stages {
        
        stage('Clone repository') {
            steps {
                git 
                  'https://github.com/deepsardana/jenkins-pipeline.git'
            }
        }
        stage('Build Image') {
            steps {
                script { 
                    dockerImage = docker.build registry + ":$BUILD_NUMBER" 
            }
        }
        stage('Testing') {
            steps {
                echo 'The Artifact will be tested'
            }
        }
        stage('Staging') {
            steps {
                echo 'The Artifact is staged onto the staging server'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'The software will now be deployed!'
            }
        }
    }    
}
