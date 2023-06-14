pipeline {
  agent {
    node {
      label 'docker'
    }

  }
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/YuvalSal99/hello-world-python.git', branch: 'master')
      }
    }

    stage('build') {
      steps {
        sleep 5
      }
    }

    stage('Test') {
      steps {
        sleep 5
      }
    }

    stage('push to dockerhub') {
      steps {
        sleep 5
      }
    }

  }
}