pipeline {
  agent none
  stages {
    stage("build & SonarQube analysis") {
      agent any
      steps {
        withSonarQubeEnv(installationName: 'sonar') {
          sh 'mvn clean package sonar:sonar'
        }
      }
    }
  }
}

