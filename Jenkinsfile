pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh './mvnw clean package'
      }
    }
    stage('Deploy') {
      steps {
        sh 'scp -o StrictHostKeyChecking=no target/Api-Investimentos-*.jar ubuntu@18.219.15.116:~/projects/api-investimentos/'
      }
    }
  }
}
