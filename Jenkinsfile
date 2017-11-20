pipeline {
  agent any
  triggers {
    cron('* * * * *')
  }
  stages {
    stage('MailTest') {
      steps {
        sh 'echo date'
        mail(subject: 'Test-Mail', body: Hi this one I was using for the testing purpose only. I was tersing multi line testing mails. Lets see what will happen with this .'Version : ${env.BuildNumber} ; version1 : ${env.DeployVersion}', to: 'somasekhar.kuruva@riversand.com', cc: 'somasekhar.kuruva@riversand.com')
      }
    }
  }
  environment {
    KEY_FOLDER_PATH = '/var/lib/jenkins/keys/'
    KEY_FILE_NAME = 'riversand-east-1.pem'
    REMOTE_SERVER = 'ubuntu@54.210.14.231'
  }
}

