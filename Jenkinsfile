pipeline {
    agent any
    	stages{
		stage ('Deploy package-maven-project'){
            		steps {
                	build job: 'package-maven-project' 
			}
		}

		stage ('Deploy to Staging'){
            		steps {
                	build job: 'deploy-to-staging' 
			}
		
		}
		post {
                	success {
                    	echo 'Now Archiving...'
			}
		}
	}       	
}

	