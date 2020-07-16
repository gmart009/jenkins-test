pipeline {
      agent any
      stages {
            stage('tidy') {
                  steps {
                     sh tidy -q -e *.html
                  }
            }
           stage('Upload to AWS') {
               steps {
                  withAWS(credentials: 'AWS-Jenkins-AIM', region:'us-east-2') {
                        s3Upload(file:'index.html', bucket:'awsjenkins123', path:'path/to/read/')
                  }
               }
          }
     }
}
