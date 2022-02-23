pipeline {
  agent any
  stages {
    stage('compile-the-app') {
      steps {
        echo 'this is the Compile job'
        sh 'npm install'
      }
    }

    stage('test-the-app') {
      steps {
        echo 'this is the Test job'
        sh 'npm test'
        sleep 9
      }
    }

    stage('package-the-app') {
      steps {
        echo 'this is the Package job'
        sh 'npm run package'
        sleep 7
      }
    }

    stage('archive-app') {
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
      echo 'THe Pipeline has successfully been completed'
    }

  }
}