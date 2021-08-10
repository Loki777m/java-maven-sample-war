pipeline{
  agent any
  stages{
    stage("Git Checkout"){
      steps{
            git credentialsId: 'github-cred-id', url: 'https://github.com/Loki777m/java-maven-sample-war.git'
           }
        }
    stage('SonarQube Analysis') {
       steps{
	 def mvn = tool 'mymaven';
         withSonarQubeEnv() {
         sh "${mvn}/bin/mvn sonar:sonar"
	      }
      }
    }
    stage("Maven Build"){
       steps{
            sh "mvn clean package"
          }
        }
      }
    }
