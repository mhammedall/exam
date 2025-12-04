pipeline {
  agent any
  stages {
    stage('Clone') {
      steps { checkout scm }
    }
    stage('Install') {
      steps { sh 'npm install' }
    }
    stage('Test') {
      steps { sh 'echo "No tests available, skipping"' }
    }
    stage('Build Docker') {
      steps { sh 'docker build -t todo-app .'}
    }
  }
  post {
    success { echo "✅ Pipeline OK" }
    failure { echo "❌ Pipeline Failed" }
  }
}
