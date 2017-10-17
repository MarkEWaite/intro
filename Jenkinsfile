pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''#!/bin/bash

echo echo built $BUILD_ID from ${GIT_REVISION:0:9} > intro.sh'''
      }
    }
    stage('Archive') {
      steps {
        archiveArtifacts(artifacts: 'intro.sh', fingerprint: true, onlyIfSuccessful: true)
      }
    }
  }
}