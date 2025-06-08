pipeline{

  agent any

  tools{
    maven 'Maven'
  }

  

  stages{
    stage('checkout'){
      steps{
      branch: 'master',url :  'https://github.com/shar4440/maven2.git'
      }
    
  }
    stage('build'){
      step{
        sh 'mvn clean package'
      }
    }

    stage('test'){
      step{
        sh 'mvn test'
      }
    }
    stage('run'){
      steps{
        sh 'java -jar target/MAVEN-1.0-SNAPSHOT.jar'
      }
    }

  }

  post{
    success{
      echo 'succeed'
    }
    failure{
      echo 'failed'
    }
  }
}
  
