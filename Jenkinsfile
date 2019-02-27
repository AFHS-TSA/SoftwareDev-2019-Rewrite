pipeline {
  agent any

  stages {
    stage('build') {
      steps {
        sh './gradlew jar'
      }
    }
  }
  post {
    success {
       telegramSend 'SoftwareDev-2019-Rewrite: Passed'
    }
    failure {
       telegramSend 'SoftwareDev-2019-Rewrite: Failed'
    }
    aborted {
       telegramSend 'SoftwareDev-2019-Rewrite: Aborted'
    }
  }
}
