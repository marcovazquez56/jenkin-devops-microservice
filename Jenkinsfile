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
	// agent any
	agent { docker { image 'maeven:3.6.3'}} 
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
