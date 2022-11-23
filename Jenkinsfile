pipeline {
  agent any
  stages {
    stage('build-the-app') {
      steps {
        echo '>>> Build Step'
        sh 'npm install'
      }
    }

    stage('test-the-app') {
      steps {
        echo '>>> Test Step'
        sh 'npm test'
      }
    }

    stage('package-the-app') {
      steps {
        echo '>>> Package Step'
        sh 'npm run package'
      }
    }

    stage('archive-artifacts') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'Tata...'
    }

  }
}