pipeline {
    agent any
  
    tools {
      gradle 'Gradle 7.2-rc-1'
    }
  
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
                sh './gradlew -v'
            }
          }
      }
    }
}
