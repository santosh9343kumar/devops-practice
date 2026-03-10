pipline {
  agent any
  stage {
    stage ('Clone Repo') {
      steps {
        git '/Users/ssantoshkumar/Documents/Learning/devops-practice'
      }
    }

    stage ('Build Docker Image') {
      steps {
        sh 'docker build -t devops-app .'
      }
    }

    stage('Run Container') {
      steps {
        sh 'docker run -d -p 5000:5000 devops-app'
      }
    }
  }
}


