pipeline {
      agent any
      stages {
           stage('Upload to AWS') {
               steps {
                  withAWS(credentials: 'AWS-Jenkins-AIM', region:'us-east-2') {
                        s3Upload(file:'index.html', bucket:'awsjenkins123', path:'path/to/read/index2.html')
                  }
               }
          }
     }
}
