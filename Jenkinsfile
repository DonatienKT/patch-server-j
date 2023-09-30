pipeline {
  agent {
    label 'ansible-server'
  }
  stages {
    stage('deploy patch playbook'){
      steps{
        dir('/home/ec2-user/ansible-det'){
          sh 'ansible-playbook patch.yml'
          sh 'ansible ws -m ping'
        }
      }
    }
    
  }
}   