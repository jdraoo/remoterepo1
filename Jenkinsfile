pipeline {
  agent any
  stages {
    stage('StageONE') {
      parallel {
        stage('StageONE') {
          steps {
            echo 'Declarative Pipeline for Demo'
            sh 'mvn clean'
          }
        }

        stage('Stage TWO') {
          steps {
            node(label: 'any') {
              echo 'From Stage TWO'
            }

          }
        }

      }
    }

    stage('Final Stage') {
      steps {
        echo 'Build Complete'
      }
    }

  }
}