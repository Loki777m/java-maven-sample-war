pipeline{
  agent any
  stages{
    stage("Git Checkout"){
      steps{
            git credentialsId: 'github-cred-id', url: 'https://github.com/Loki777m/java-maven-sample-war.git'
           }
          }
     stage("Maven Build"){
       steps{
            sh "mvn clean package"
            }
        }
      }
    }
