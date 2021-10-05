pipeline {
  agent any
  stages {
    stage('Dev Build') {
      steps {
        echo 'Dev build successful'
      }
    }

    stage('Deploy to QA') {
      steps {
        echo 'Deployed to QA Succcessfully'
      }
    }

    stage('UI Testing(Smoke)') {
      parallel {
        stage('UI Testing(Smoke)') {
          steps {
            echo 'API Test success'
          }
        }

        stage('performance test') {
          steps {
            echo 'performance test successful'
          }
        }

        stage('API Testing (Smoke)') {
          steps {
            echo 'Api test'
          }
        }

      }
    }

    stage('Deploy to QAT') {
      steps {
        echo 'depoyed to qat'
      }
    }

    stage('certify to UAT') {
      steps {
        echo 'certified to UAT'
      }
    }

    stage('Prod deploy') {
      steps {
        echo 'Deployed to Production'
      }
    }

  }
}