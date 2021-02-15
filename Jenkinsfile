pipeline {
  agent any
  stages {
    stage('Fixing File') {
      steps {
        sh 'mkdir ${WORKSPACE}/roles/nginx-install/files'
        sh 'cp ${WORKSPACE}/nginx.conf ${WORKSPACE}/roles/nginx-install/files/nginx.conf'
      }
    }

    stage('Running Playbook') {
      steps {
        ansiblePlaybook(playbook: '${WORKSPACE}/playbook.yaml', disableHostKeyChecking: true, inventory: '/ssh/inventory')
      }
    }

  }
}