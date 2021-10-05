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
            echo 'UI Test success'
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
        echo 'deployed to qat'
      }
    }

    stage('certify to UAT') {
      steps {
        echo 'certified to UAT'
        input 'Do u want to get certificate'
      }
    }

    stage('Prod deploy') {
      steps {
        echo 'Deployed to Production'
      }
    }

  }
}