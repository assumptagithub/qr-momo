

pipeline{
    agent any
    tools{
        maven 'Maven3'
    }
    stages{
        stage('clone'){
            steps{
              git branch: 'develop', credentialsId: 'personal-token', url: 'https://github.com/assumptagithub/qr-momo.git'
            sh"ls -l"  
            }
        }
        stage('Maven test'){
            steps{
                sh"mvn test"
            }
        }
        stage("Build & Test"){
            sh 'docker build -t app:v1 .'
        }
    }
}
