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
        git(url: 'https://github.com/sowmyanarayanan-sailapathi/Salesforce', branch: 'master')
        bat 'mvn -f Salesforce/pom.xml test'
      }
    }

    stage('Deploy') {
      when {
        branch 'master'
      }
      steps {
        input(id: 'Yes', message: 'Ready to Deploy')
      }
    }

  }
}