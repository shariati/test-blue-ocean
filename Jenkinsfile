pipeline {
  agent {
    node {
      label 'linux'
    }
    
  }
  stages {
    stage('Build') {
      parallel {
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
        stage('build2') {
          steps {
            sh './test'
          }
        }
      }
    }
    stage('Test') {
      steps {
        jiraComment(issueKey: '123', body: '12333')
        archiveArtifacts(artifacts: '133', allowEmptyArchive: true, defaultExcludes: true)
      }
    }
  }
  environment {
    test = ''
    test2 = ''
  }
}