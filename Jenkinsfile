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
        sh '\'\' docker build -t yuvalsal/hello-world-python:${env.BUILD_NUMBER} . \'\''
      }
    }

    stage('Test') {
      steps {
        sh 'docker run -itd --name python -p 8080:8080 python'
        sleep 5
        sh 'curl localhost:8080'
        sh 'docker stop python && docker rm python'
      }
    }

    stage('push to dockerhub') {
      steps {
        sleep 5
      }
    }

  }
}