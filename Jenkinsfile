pipeline {
  agent {
    node {
      label 'Node'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        echo 'Build Stage message'
        archiveArtifacts(artifacts: 'test', allowEmptyArchive: true)
      }
    }
  }
}