pipeline {
	agent any
	stages {
		stage('Upload to S3') {
			steps {
				sh 'echo "Hello Jenkins"'
				withAWS(region:'us-east-2',credentials:'aws-static') {
						s3Upload(pathStyleAccessEnabled:true,payloadSigningEnabled:true,file:'index.html',bucket:'jenkins-playground')
				}
			}
		}
	}
}