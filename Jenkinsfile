pipeline{
	agent any
	stages{
		stage('Checkout'){
			steps{
				checkout scm
			}
		}
		stage('Compile'){
			steps{
				sh 'mvn compile'
			}
		}
		stage('Test'){
			steps{
				sh 'mvn test'
			}
		}
		stage('Package'){
			steps{
				sh 'mvn package -DskipTests'
			}
		}
		stage("Achive Artifact"){
			steps{
				archiveArtifacts artifacts:'target/*.jar',fingerprint: true
			}
		}
		stage('Deploy'){
			steps{
				sh 'cp target/*.jar otp/First-Proj/'
			}
		}

	}
}
