pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing...'
        sh 'ls -l .'
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