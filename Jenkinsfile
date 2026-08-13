pipeline{
	agent any
	stages{
		stage('get_con'){
			steps{
				git branch:'main',
				url:'https://github.com/Deepakumar155/First_Proj'
			}
		}
		stage('Build & test'){
			steps{
				sh 'mvn clean test'
			}
		}
	}
}
