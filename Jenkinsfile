pipeline {
  agent any
  stages {
    stage('Check Code') {
      steps {
        git(url: 'https://github.com/Ismail10001/jenkins-test', branch: 'main')
      }
    }

    stage('Log') {
      steps {
        sh 'ls -la'
      }
    }

    stage('Deploy') {
      steps {
        sh 'sh \'sshpass -p "iot@12345678" scp -r * iotuser@51.120.241.53:/var/www/html/\''
      }
    }

  }
}