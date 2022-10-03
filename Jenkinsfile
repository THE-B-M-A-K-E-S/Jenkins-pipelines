pipeline {
    agent any
    
    stages {
        stage('Pulling from git...'){
            steps{
               git branch : 'main',
                url : 'https://github.com/THE-B-M-A-K-E-R-S/Jenkins-pipelines'
            }
        }
        
        stage('MVN CLEAN'){
            steps {
                sh """MVN CLEAN"""
            }
        }
        
        stage('Show system date..'){
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
