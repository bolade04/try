pipeline {
  agent {
    node {
      label 'docker'
    }

  }
  stages {
    stage('Git') {
      steps {
        git(url: 'https://github.com/bolade04/try', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        sh 'docker build -t bolade4/try_new .'
      }
    }

    stage('Docker Login') {
      steps {
        sh 'docker login -u bolade4 -p dckr_pat_H5QLaPXby3W8vtnZh-iR4WliPD0'
      }
    }

    stage('Docker Push') {
      steps {
        sh 'docker push bolade4/try_app'
      }
    }

  }
}