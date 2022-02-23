pipeline {
  agent any
  stages {
    stage('compilation') {
      steps {
        echo 'this is the compile job'
        sh 'npm install'
      }
    }

    stage('testing') {
      steps {
        echo 'this is the test job'
        sh 'npm test'
      }
    }

    stage('packaging') {
      steps {
        echo 'this is the package job'
        sh 'npm run package'
      }
    }

    stage('archiving') {
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
      echo 'pipeline created via code..by antony..'
    }

  }
}