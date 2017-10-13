pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }
    stage('Monitor') {
      parallel {
        stage('Test') {
          steps {
            echo 'Testing...'
          }
        }
        stage('') {
          steps {
            echo 'Monitoring progress...'
            pwd(tmp: true)
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