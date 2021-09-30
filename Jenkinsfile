pipeline{
	agent any
	stages {
		stage('GIT CHECKOUT'){
			steps{
				git 'https://github.com/sachinmr2151997/maven-project.git'
			}
		}
		stage('COMPILATION'){
			steps {
				sh 'mvn clean install'	
		}	
	}			
		stage('DEPLOY'){
			steps {
			sshagent(['deploy']) {
                        sh 'scp -o StrictHostKeyChecking=no webapp/target ec2-user@172.31.30.243:/opt/apache-tomcat-8.5.71/webapps'
                               }
			}
		}
  }
}
