pipeline {
    agent any
  environment{
    AWS_DEFAULT_REGION= 'Asia Pacific (Mumbai) ap-south-1'

  AWS_ACCESS_KEY_ID= 'AKIAS4H3K6VC6G4EYL4G'

   AWS_SECRET_ACCESS_KEY='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'
  }
    stages {
        stage('deploy') {
            steps {
                echo 'depoloy'
              sh "aws configure set region $AWS_DEFAULT_REGION" 
              sh "aws configure set aws_access_key_id $AWS_ACCESS_KEY_ID"  
              sh "aws configure set aws_secret_access_key $AWS_SECRET_ACCESS_KEY"
              sh "aws s3 cp /var/lib/jenkins/workspace/s3  s3://vishnu-12"
            }
        }
    }
}
