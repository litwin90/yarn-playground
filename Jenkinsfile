#!groovy

import groovy.json.JsonOutput
@Library('jenkins-lib')_

buildSteps.agent {
    stage('Check out') {
        buildSteps.checkout([
            branch: env.GIT_BRANCH,
            credentialsId: credentials.gitlabUser(),
            url: env.GIT_URL,
        ])
    }
    def GTM_ID = GTM_AUTH_QA = GTM_ENV_QA = GTM_AUTH_DEV = GTM_ENV_DEV = GA_ENABLED = null;

   

  
   
   
  
    def tag = imagesNames.getImageTag(env.GIT_BRANCH, env.BUILD_ID)
    
    stage('Update CI description') {
        currentBuild.description = "${tag}"
    }
}
