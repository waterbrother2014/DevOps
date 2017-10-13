pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }
    stage('Test') {
      parallel {
        stage('Testing') {
          steps {
            echo 'Testing...'
          }
        }
        stage('Monitoring') {
          steps {
            pwd()
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
        ansiblePlaybook(installation: 'Default', playbook: '/home/david/git/DevOps/Ansible/playbook/main.yml')
      }
    }
  }
}