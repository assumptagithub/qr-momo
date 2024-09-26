
pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                'https://github.com/assumptagithub/qr-momo.git'
            }
        }
        stage('Build Docker Image'){
            steps{
                script{
                    // Build the Docker image
                    sh 'docker build -t momo-app .'
                }
            }
        }
    }
}























