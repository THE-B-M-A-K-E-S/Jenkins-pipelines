pipeline {
    agent any
    
    stages {
        stage('Pulling from git...'){
            steps{
               git branch : 'main',
                url : 'https://github.com/THE-B-M-A-K-E-R-S/Jenkins-pipelines'
            }
        }
        
        stage('Testing maven...'){
            steps {
                sh """mvn -versinon"""
            }
        }
        
        stage('Show system date.....'){
            steps{
               script {
                    DATE_TAG = java.time.LocalDate.now()
                    DATETIME_TAG = java.time.LocalDateTime.now()
                }
                sh "echo ${DATETIME_TAG}"
            }
        } 
   }
}
