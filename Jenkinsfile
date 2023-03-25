pipeline {
    agent any

    stages {
        stage('cicd') {
            steps {
                sh '''
                aws ecr get-login-password --region us-east-2 | docker login --username AWS --password-stdin 101045478775.dkr.ecr.us-east-2.amazonaws.com
                dokcer build -t 01045478775.dkr.ecr.us-east-2.amazonaws.com/today-ecr:latest .
                docker push 101045478775.dkr.ecr.us-east-2.amazonaws.com/today-ecr:latest
                '''
            }
        }
    }
}
