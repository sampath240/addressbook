pipeline{
	agent any
	tools{
		maven 'maven'
	}
	stages{
		stage('checkout'){
			steps{
				git 'https://github.com/sampath240/addressbook.git'
			}
		}
		stage('Build'){
			steps{
				sh 'mvn clean compile'
			}
		}
		stage('package'){
			steps{
				sh 'mvn package'
			}
		}
	}
}
