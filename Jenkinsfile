pipeline {
  agent any
  triggers {
    cron('* * * * *')
  }
  stages {
    stage('MailTest') {
      steps {
        sh 'echo date'
        mail(subject: 'Test-Mail', body: Testing multi line mailing here. Here I;m adding multi lines for the this multi line testing. So lets see for it. 'Version : ${env.BuildNumber} ; version1 : ${env.DeployVersion}', to: 'somasekhar.kuruva@riversand.com', cc: 'somasekhar.kuruva@riversand.com')
      }
    }
  }
  environment {
    KEY_FOLDER_PATH = '/var/lib/jenkins/keys/'
    KEY_FILE_NAME = 'riversand-east-1.pem'
    REMOTE_SERVER = 'ubuntu@54.210.14.231'
  }
}
