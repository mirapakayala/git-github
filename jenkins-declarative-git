pipeline{
    agent any
    
    environment{
        PATH = /home/ec2-user/apache-maven-3.6.3/bin:$PATH"
        }
    stages{
        stage("Git checkout"){
            steps{
                git credentialsId: 'gitHub' , url: 'https://github.com/mirapakayala/git-github.git'
            }
        }
        stage("Maven build"){
           steps{
              sh "mvn clean package"
          }
       }
    }
}
