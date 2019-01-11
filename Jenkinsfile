pipeline {
  agent any

  options {
    copyArtifactPermission(projectNames: 'horizon-kolla/*')
  }

  stages {
    stage('package') {
      steps {
        sh "git archive --output=horizon-theme.tar ${env.BRANCH_NAME}"
        archiveArtifacts(artifacts: 'horizon-theme.tar', onlyIfSuccessful: true)
      }
    }
  }
}
