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
		stage('TEST'){
			steps {
			sh 'echo this is my 2nd pipeline job'
			sh 'du -h'
			}
		}
  }
}
