pipeline {
 agent any
 stages {
  stage('Checkout') {
   steps {
    git credentialsId: 'userId', url: 'https://github.com/Kragada/EnvironmentDemo', branch: 'main'
   }
  }
  stage('Restore PACKAGES') {
   steps {
    bat "dotnet restore"
   }
  }
  stage('Build') {
   steps {
    bat 'dotnet build'
   }
  }
