pipeline {
  agent any
  stages {
    stage('Test-ENV') {
      parallel {
        stage('Test-ENV') {
          steps {
            sh 'echo "HI test is successfull."'
          }
        }
        stage('Demo-ENV') {
          steps {
            build 'test-1'
            sh 'echo "This is demo test."'
          }
        }
      }
    }
    stage('Prod-ENV') {
      steps {
        sh 'echo \'This is Prod test\''
      }
    }
  }
}