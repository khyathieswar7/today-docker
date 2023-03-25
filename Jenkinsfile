pipeline {
    agent any

    stages {
        stage('cicd') {
            steps {
                sh '''
                aws ecr get-login-password --region us-east-2 | sudo  docker login --username AWS --password-stdin 101045478775.dkr.ecr.us-east-2.amazonaws.com
                sudo docker build -t 101045478775.dkr.ecr.us-east-2.amazonaws.com/today-ecr:latest .
                sudo docker push 101045478775.dkr.ecr.us-east-2.amazonaws.com/today-ecr:latest
                '''
            }
        }
    }
}
