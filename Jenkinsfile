pipeline {
  agent any
  stages {
    stage('Change directory to marlin') {
      steps {
        dir(path: '/home/czacha/PlatformIO/Marlin') {
          sh 'git pull'
        }

      }
    }

    stage('build with PlatformIO') {
      steps {
        sh 'docker run --rm -ti -v /home/czacha/PlatformIO/Marlin:/opt/workspace suculent/platformio-docker-build'
      }
    }

    stage('Complete') {
      steps {
        echo 'Build completed.'
      }
    }

  }
}