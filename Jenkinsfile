pipeline {
  agent any
  stages {
    stage('stage1') {
      agent any
      steps {
        sh '''pwd
date'''
      }
    }

    stage('stage2') {
      parallel {
        stage('stage2') {
          steps {
            echo 'this is stage 2'
          }
        }

        stage('concurrunt') {
          steps {
            sh '''ls 
pwd'''
          }
        }

      }
    }

    stage('stage3') {
      steps {
        echo 'this is stage 3'
      }
    }

    stage('stage-4') {
      steps {
        sh '''pwd
'''
        echo 'this is final stage'
      }
    }

  }
}