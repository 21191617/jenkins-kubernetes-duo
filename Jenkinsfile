pipeline {
    agent any
    environment {

    }
    stages {
        stage('Deploy App') {
            steps {
                sh '''
                kubectl apply -f ./k8s-deployments
                kubectl rollout restart deployment flask-deployment
                '''
            }
        }
        stage('Deploy NGINX') {
            steps {
                sh '''
                kubectl apply -f ./k8s-deployments
                kubectl rollout restart deployment nginx
                '''                
            }
        }
    }
}