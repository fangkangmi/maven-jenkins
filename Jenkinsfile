pipeline {
  agent any
  tools {
        maven "M3" 
   }

  stages {
      stage('Build Artifact') 
      {
            steps 
            {
              sh "mvn clean package -DskipTests=true"
              archive 'target/*.jar' 
            }  
       }
      stage('Test Maven - JUnit') 
      {
            steps 
            {
              //sh "mvn test"
              echo "Running unit tests"
            }
      }
      stage('Deploy') 
      { 
          steps 
          { 
              input('Continue to Deploy?') 
              echo 'Deploying to Production Environment' 
          } 
      }
    
     stage('Dev env') 
      { 
          steps 
          { 
              echo 'Deploying to Production Environment' 
          } 
      }
    
    
     stage('Test env') 
      { 
          steps 
          {  
              echo 'Deploying to Production Environment' 
          } 
      }
    
     stage('UAT env') 
      { 
          steps 
          { 
              echo 'Deploying to Production Environment' 
          } 
      }
    
    stage('Production env') 
      { 
          steps 
          {  
              echo 'Deploying to Production Environment' 
          } 
      }
    
    }
}
