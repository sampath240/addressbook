pipeline{
	tools{
		maven 'M3'
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
		stage('Test'){
			steps{
				sh 'mvn test'
				junit '**/target/surefire-reports/Test-*.xml'
			}
		}
		stage('package'){
			steps{
				sh 'mvn package'
			}
		}
	}
