//SCRIPTED PIPELINE (STAGE BLOCKS ARE OPTIONAL)
//DECLARATIVE (all your tasks in STAGES, We cannot have any pipeline without stages )
pipeline {
	//agent any
	agent { docker { image 'maven:3.6.3'} }
	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
				echo "Build"	
			}
		}
		stage('Test') {
			steps {	
				echo "Test"	
			}
		}	
		stage('Integration Test') {
			steps {
				echo "Integration Test"		
			}
		}
	} 
	
	post  {
		always {
			echo 'Im awesome. I run always'
		}		
		success {
			echo 'I run when your are sucessful'
		}		
		failure {
			echo 'I run when you fail'
		}
	}				
 }
		
