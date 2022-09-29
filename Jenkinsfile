pipeline{
  agent any 
  tools {
    maven "maven3.8.6"
  }  
  stages {
    stage('1GetCode'){
      steps{
        sh "echo 'cloning the latest application version' "
        git credentialsId: 'github', url: 'https://github.com/eSGee12/maven-web-application.git'
      }
    }
    stage('3Test+Build'){
      steps{
        sh "echo 'running JUnit-test-cases' "
        sh "echo 'testing must passed to create artifacts ' "
        sh "mvn clean package"
      }
    }
    /*
    stage('4CodeQuality'){
      steps{
        sh "echo 'Perfoming CodeQualityAnalysis' "
        sh "mvn sonar:sonar"
      }
    }
    stage('5uploadNexus'){
      steps{
        sh "mvn deploy"
      }
    } 
    stage('8deploy2prod'){
      steps{
        deploy adapters: [tomcat8(credentialsId: 'tomcatcredentials', path: '', url: 'http://3.87.145.20:8080/')], contextPath: null, war: 'target/*war'
      }
    }
}
  post{
    always{
      emailext body: '''Hello Folks,
Congratulations on the successful deployment
Regards.
Olusegun (SG)
Senior Lead Dev Eng''', subject: 'App Deployed', to: 'segundaremail@gmail.com, dareesgee@gmail.com'
    }
    success{
      emailext body: '''Hello Folks,
Congratulations on the successful deployment
Regards.
Olusegun (SG)
Senior Lead Dev Eng''', subject: 'App Deployed', to: 'segundaremail@gmail.com, dareesgee@gmail.com'
    } 
    failure{
      emailext body: '''Hello Folks,
Congratulations on the successful deployment
Regards.
Olusegun (SG)
Senior Lead Dev Eng''', subject: 'App Deployed', to: 'segundaremail@gmail.com, dareesgee@gmail.com'
    }
  } 
  */
}
}
