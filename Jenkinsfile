pipeline {
  agent any

  options {
    copyArtifactPermission(projectNames: 'horizon-kolla/*')
  }

  stages {
    stage('package') {
      steps {
        sh 'git archive --output=horizon-theme.tar .'
        archiveArtifacts(artifacts: 'horizon-theme.tar', onlyIfSuccessful: true)
      }
    }
  }
}
