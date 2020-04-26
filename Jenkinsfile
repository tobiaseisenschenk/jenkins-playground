pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				sh 'echo "Hello Jenkins"'
				sh '''
					withAWS(region:'us-east-2',credentials:'aws-static') {
						s3Upload(file:'index.html',bucket:'jenkins-playground')
					}

				'''
			}
		}
	}
}