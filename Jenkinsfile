pipeline {
  agent any
  stages {
    stage('plan') {
      steps {
        echo 'plan for pipeline'
      }
    }

    stage('code') {
      steps {
        echo 'prepare code'
      }
    }

    stage('Build') {
      steps {
        echo 'Build code for pipeline'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Test code'
          }
        }

        stage('Release') {
          steps {
            echo 'Release code'
          }
        }

        stage('Deploy') {
          steps {
            echo 'Deploy code'
          }
        }

        stage('Operation') {
          steps {
            echo 'Operate code'
          }
        }

      }
    }

  }
}