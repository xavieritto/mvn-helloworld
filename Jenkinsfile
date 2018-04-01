pipeline {
  agent any    

  
  stages {
    stage('Clone repository') {
      steps {
        checkout scm
      }
    }
    stage('Build') {
      steps {
		sh 'cd my-app && chmod +x mvnw && ./mvnw clean compile package'
      }
    }
  }
  post {
    always {
      sh 'cd my-app && chmod +x mvnw && ./mvnw clean'      
    }    
  }
}

