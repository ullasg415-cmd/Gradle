pipeline{
       agent any
       tools{
       gradle 'gradle'
       jdk 'JDK'
       }
       stages{
       	stage('Checkout'){
       	   steps{
       	     git branch:'main',url:'https://github.com/ullasg415-cmd/Gradle.git'
       	     }
       	    }
       	 stage('Build'){
       	 steps{
       	 sh'gradle build'
       }
      }
        stage('Test'){
        steps{
        sh'gradle test'
        }
      }
      stage('Run Application'){
      steps{
       sh'gradle run'
       }
     }
    }
    post{
     success{
     echo'Build and Deployment succesfull'
     }
     failure{
       echo'Build failure'
       }
     }
   }
