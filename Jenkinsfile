pipeline {
  agent any
  stages {
      stage("run frontend") {
          steps {
            echo 'executing yarn...'
            nodejs('NodeJS 10.17.0') {
                sh 'yarn install'
            }
          }
      }
      stage("run backend") {
          steps {
            echo 'executing Gradle...'
            withgradle() {
                sh './gradlew -v'
            }
          }
      }
  }
}
