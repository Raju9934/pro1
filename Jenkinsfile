pipeline {
    agent any
    stages{
        stage('build project'){
            steps{
                git url:'https://github.com/Raju9934/pro1.git', branch: "master"
                sh 'mvn clean package'
              
            }
        }
        stage('Build docker image'){
            steps{
                script{
                    sh 'docker build -t 2024dock/staragileprojectfinance:v1 .'
                    sh 'docker images'
                }
            }
        }
         
        
     stage('Deploy') {
            steps {
                sh 'sudo docker run -itd --name My-first-containe21211 -p 8091:8091 2024dock/staragileprojectfinance:v1'
                  
                }
            }
        
    }
}
