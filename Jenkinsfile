pipeline {
  agent any
  
 stages {  
  stage('Unit Tests') {
      steps {
        sh 'ant -f test.xml -v'
        junit 'reports/result.xml'
      }
  }
        
  stages {
    stage('build') {
      steps {
        sh 'ant -f build.xml -v'
      }
    }
  }
  
  post { 
    always {
      archive 'dist/*.jar'
    }
  }
}

  
