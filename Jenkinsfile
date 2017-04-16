pipeline {
  agent any
  stages {
    stage('Devl') {
      steps {
        parallel(
          "Devl": {
            echo 'Hello'
            
          },
          "Build": {
            echo 'Echo "Compile\''
            
          },
          "Compile": {
            echo 'echo \'compile\''
            
          }
        )
      }
    }
    stage('Scan') {
      steps {
        parallel(
          "Scan": {
            echo 'Scan'
            
          },
          "UnitTest": {
            echo 'Unit Testing'
            
          }
        )
      }
    }
    stage('TestDeploy') {
      steps {
        echo 'Test Deploy'
      }
    }
    stage('FunctionalTest') {
      steps {
        parallel(
          "FunctionalTest": {
            echo 'FunctionalTesting'
            
          },
          "PerformanceTest": {
            echo 'Performance Testing'
            
          },
          "SecureTest": {
            echo 'SecureTest'
            
          }
        )
      }
    }
    stage('ProdDeploy') {
      steps {
        echo 'Production Deploy'
      }
    }
  }
}