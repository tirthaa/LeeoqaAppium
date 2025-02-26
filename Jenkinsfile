pipeline{
	agent any
	stages{
		stage("Start Grid"){
			steps{
				sh "docker-compose up -d"
				}
			}
		}
	post{
		always{
			archiveArtifacts artifacts: 'output/**'
			sh "docker-compose down"			
		}
	}
}
