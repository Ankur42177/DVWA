pipeline {
	agent any
	stages {
		stage ("Git checkout"){
			steps {
				git branch: "master",
					url: "https://github.com/Ankur42177/DVWA.git"
				sh "ls"
			}
		}

		stage ("sonar-publish"){
			steps {
				echo "===========Performing Sonar Scan============"
				sh "${tool("SonarQube_Scanner")}/bin/sonar-scanner"
			}
		}
//         stage ("Dynamic Analysis - DAST with OWASP ZAP") {
// 			steps {
// 				sh "docker run -t owasp/zap2docker-stable zap-baseline.py -t http://10.54.1.240:5050/ || true"
// 			}
		
// 		}
		
	}
}
