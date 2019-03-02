pipeline{
	agent { docker "maven:3.6.0-alpine" }
	stages{
		stage('Checkout'){
			steps{
				git "https://github.com/sudhakarkappala/spring-petclinic.git"
			}
		}
		stage('Build'){
			sh "mvn clean package"
			junit "**/target/surefire-reports/TEST-*.xml"
		}
	}
}