pipeline {
	agent any
	stages {
		stage('Compile') {
			steps {
				sh 'chmod +x gradle'
				sh './gradlew compileJava'
			}
		}
		stage('Unit test') {
			steps {
				sh './gradlew test'
			}
		}
		stage('Code coverage') {
			steps {
				sh './gradlew jacocoTestReport'
				sh './gradlew jacocoTestCoverageVerification'
			}
		}
	}
}
