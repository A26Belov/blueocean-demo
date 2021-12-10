pipeline {
  agent any
  stages {
    stage('checkOutgit') {
      steps {
        git(url: 'git@github.com:A26Belov/ansible.git', branch: 'main', poll: true, credentialsId: '3bca6740-84c9-4ef0-acb3-75be1a80d240')
      }
    }

    stage('Build') {
      steps {
        echo 'Build'
      }
    }

    stage('Deploy-1') {
      parallel {
        stage('Deploy-1') {
          steps {
            sleep(unit: 'SECONDS', time: 10)
            echo 'Deploy-1'
          }
        }

        stage('Deploy-2') {
          steps {
            sleep 15
            echo 'Deploy-2'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
      }
    }

  }
}