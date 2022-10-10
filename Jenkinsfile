pipeline {
  agent none
  stages {
    stage("build & SonarQube analysis") {
      agent any
      steps {
        withSonarQubeEnv(installationName: 'sonar') {
          sh 'mvn -f maven-app/pom.xml clean package sonar:sonar'
        }
      }
    }
  }
}

