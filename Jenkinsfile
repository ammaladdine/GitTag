pipeline{
  stages{
    stage("checkout"){
      steps{
          checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'achyuth', url: 'https://github.com/ammaladdine/GitTag.git']]])
         }
       }
    stage("checkout"){ 
      steps{
        script{
          sh """
            mvn clean
            mvn install
          """
        }
      }
    }
  }
}  
