pipeline {
  agent any
  stages {
    stage('Development') {
      steps {
        echo 'Development Completed'
      }
    }

    stage('Smoke Test') {
      steps {
        git(url: 'https://github.com/sowmyanarayanan-sailapathi/ACMEBuild', branch: 'master')
        bat 'mvn test'
      }
    }

    stage('Deploy') {
      steps {
        input(id: 'Yes', message: 'Ready to Deploy')
      }
    }

  }
}