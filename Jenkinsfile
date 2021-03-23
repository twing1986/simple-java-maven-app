pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
		}
	}
	environment {
		PATH = "/usr/local/bin:${env.PATH}"
	}		
    stages {
        stage('Build') {
            steps {
				echo 'Hello!'
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
