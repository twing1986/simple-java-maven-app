pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
		}
	}
	tools { 
        maven 'Maven 3.6.3' 
    }
	environment {
		PATH="/sbin:/usr/sbin:/usr/bin:/usr/local/bin:/bin"
	}		
    stages {
        stage('Build') {
            steps {
				echo 'Hello!'
				sh 'mvn --version'
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
