// SCRIPTED
// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 		stage('Integration Test') {
// 		echo "Test"
// 	}
// }

// DECLARATIVE
pipeline {
	agent any
	// agent { docker { image 'maven:3.6.3'}} 
	stages {
		stage('Build') {
			steps {
				// sh 'mvn --version'
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $end.BUILD_NUMBER"
				echo "BUILD_ID - $end.BUILD_ID"
				echo "JOB_NAME - $end.JOB_NAME"
				echo "BUILD_TAG - $end.BUILD_TAG"
				echo "BUILD_URL - $end.BUILD_URL"
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
	post {
		always {
			echo "I am awesome. I run always"
		}
		success {
			echo "I run when you're successful"
		}
		failure {
			echo "I should not be running, you're wrong!"
		}
	}
}
