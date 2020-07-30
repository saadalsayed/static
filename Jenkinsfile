pipeline {
    agent any
    stages {
       steps {
                withAWS(region:'us-west-2',credentials:'test') {
                  sh 'echo "Uploading content with AWS creds"'
                      s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkinsbucketest')
                  }
              }
    }
}
