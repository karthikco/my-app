node{
  stage('SCM Checkout'){
     
    git 'https://github.com/karthikco/my-app'
  }
  stage('Compile-Package'){
    //Get maven home path
    def mvnHome = tool name: 'maven-3', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
  
  stage('Email Notification'){
  mail bcc: '', body: '''Hi these are jenkins job alerts
thanks
Karthik''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'karword@gmail.com'

  }
  stage('Slack Notification'){
  slackSend baseUrl: 'https://hooks.slack.com/services/',
    channel: '#jenkins-pipeline-demo',
    color: 'good', 
    message: 'welcome to Slack,Jenkins!',
    teamDomain: 'agencybill',
    tokenCredentialId: 'slack-demo'

  }
}
