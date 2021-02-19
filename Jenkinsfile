pipeline {
  agent any
  
  stages {
    stage('Setup') {
      steps {
        sh 'echo $JAVA_HOME=$(JAVA_HOME)'
        git url: 'https://github.com/CristhianFG/hello-spring_gradle.git', branch:'main'
      }
    }
    stage('Build') {
      steps {
        withGradle {
          sh './gradlew assemble'
        }
      }
    }
  }
}
