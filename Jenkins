pipeline {
  agent any

  stages {
    stage('Clone Repo') {
      steps {
        echo '📥 Cloning Repository...'
        git url: 'https://github.com/octocat/Hello-World.git', branch: 'master'
      }
    }

    stage('List Files') {
      steps {
        echo '📂 Listing project files...'
        sh 'ls -l'
      }
    }

    stage('Display File Content') {
      steps {
        echo '📄 Showing contents of README'
        sh 'cat README'
      }
    }

    stage('Success Message') {
      steps {
        echo '✅ Jenkins pipeline ran successfully!'
      }
    }
  }

  post {
    always {
      echo '🔁 Pipeline execution completed.'
    }
    success {
      echo '🎉 Success!'
    }
    failure {
      echo '🔥 Failed!'
    }
  }
}
