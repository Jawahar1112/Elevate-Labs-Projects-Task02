pipeline {
  agent any

  environment {
    IMAGE = "elevate-task2"
    TAG   = "${env.BUILD_NUMBER}"
  }

  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/Jawahar1112/Elevate-Labs-Projects-Task02.git'
      }
    }

    stage('Build Docker Image') {
      steps {
        sh "docker build -t ${IMAGE}:${TAG} ."
      }
    }

    stage('Run Tests') {
      steps {
        // Adjust this to your actual test command
        sh "docker run --rm ${IMAGE}:${TAG} sh -c './run-tests.sh'"
      }
    }

    stage('Deploy') {
      when { branch 'main' }
      steps {
        echo "Deploying ${IMAGE}:${TAG} (replace this with real deploy steps)"
      }
    }
  }

  post {
    always {
      cleanWs()
    }
  }
}
