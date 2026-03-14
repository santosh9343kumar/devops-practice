pipline {
  agent any
  stage {
    stage ('Clone Repo') {
      steps {
        git 'git@github.com:santosh9343kumar/devops-practice.git'
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


