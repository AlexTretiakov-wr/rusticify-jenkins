pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        sh 'sh "cargo test src/main.rs"'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
        sh 'cargo test'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying'
        sh 'Jenkins/deploy.sh'
      }
    }

  }
}