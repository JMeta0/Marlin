pipeline {
  agent any
  stages {
    stage('Change directory to marlin') {
      agent any
      steps {
        dir(path: '/Marlin') {
          sh 'git pull'
        }

      }
    }

    stage('Complete') {
      steps {
        echo 'Build completed.'
      }
    }

  }
}