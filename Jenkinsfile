pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        git branch: 'main', url: 'https://github.com/Jawahar1112/Elevate-Labs-Projects-Task02.git'
      }
    }

    stage('Build Docker Image') {
      steps {
        echo "Building Docker Image..."
      }
    }

    stage('Run Tests') {
      steps {
        echo "Running Tests..."
      }
    }

    stage('Deploy') {
      steps {
        echo "Deploying..."
      }
    }
  }
}
