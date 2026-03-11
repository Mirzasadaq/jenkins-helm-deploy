pipeline {
  agent any
    stages {
      stage('Build maven'){
        steps {
          sh 'pwd'
          sh 'mvn clean install package'
        }
      }
      stage('copy Artifact'){
        steps {
          sh 'pwd'
          sh 'cp -r target/*.jar docker'
        }
      }
      stage('Run Test'){
        steps {
          sh 'mvn test'
        }
      }
    }
}