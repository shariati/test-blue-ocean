pipeline {
  agent {
    node {
      label 'Node'
    }
    
  }
  stages {
    stage('Build') {
      environment {
        stageVar1 = '123'
        stageVar2 = '234'
      }
      steps {
        echo 'Build Stage message'
        archiveArtifacts(artifacts: 'test', allowEmptyArchive: true)
      }
    }
  }
  environment {
    test = ''
    test2 = ''
  }
}