pipeline {
	agent any

	stages {
		stage('fetch code') {
			steps {
				git branch: 'main', url: 'https://github.com/pathakbhaskar/sampleapp.git'
			}
		}
		stage('Install Apache') {
			steps {
				sh 'sudo apt install apache2 -y'
			}
		}
		stage('Deploy App') {
			steps {
				sh 'sudo cp -R * /var/www/html/'
			}
		}
	}
}
