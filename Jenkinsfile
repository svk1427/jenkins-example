pipeline {
	agent { label 'linux-node' }
	stages {
		stage('---clean---'){
			steps {
				tool name: 'maven3.3.3', type: 'maven'
				sh "mvn clean"
			}
		}
		stage('---test---') {
			steps {
				tool name: 'maven3.3.3', type: 'maven'
				sh "mvn test"
			}
		}
		stage('---package---'){
			steps {
				tool name: 'maven3.6.3', type: 'maven'
				sh "mvn package"
			}
		}
	}
}
