pipeline {
  agent any
  environment {
    DOCKERHUB_CREDENTIALS= credentials('moabdelaziz-dockerhub')
  }
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t moabdelaziz1/test-jenk-img .'
      }
    }
    stage('Run') {
      steps {
        sh 'docker compose up -d'
      }
    }
    stage('Login') {
      steps {
        sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
      }
    }
    stage('DockerPush') {
      steps {
        sh 'docker push moabdelaziz1/test-jenk-img .'
      }
    }
  }
  post {
    always {
      sh 'docker logout'
    }
  }
}
