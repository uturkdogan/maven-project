pipeline {
	agent any
	stages {
		steps {
			sh 'mvn clean package'
		}
		post {
			success {
				echo 'Now Archiving..'
				archiveArtifacts artifacts: '**/target/*.war'
			}
		}
	}
}
