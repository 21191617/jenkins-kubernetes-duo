pipeline {
    agent any
    stages {
        stage('Deploy App') {
            steps {
                sh '''
                kubectl apply -f 
                kubectl rollout restart deployment flask-deployment
                '''
            }
        }
        stage('Deploy NGINX') {
            steps {
                sh '''
                kubectl apply -f 
                kubectl rollout restart deployment nginx
                '''                
            }
        }
    }
}