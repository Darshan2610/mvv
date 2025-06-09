pipeline{
	agent any
	tools{maven 'maven'}
	stages{
	    stage('checkout'){
	        steps{git branch:'master',url:'https://github.com/Darshan2610/mvv.git'}
	    }
	    stage('build'){
	    steps{sh 'mvn clean package'}
	    }
	    
	    stage('testing'){
	        steps{sh 'mvn test'}
	    }
	    
	    stage('running'){
	        steps{sh 'java -jar target/mvv-1.0-SNAPSHOT.jar'}
	    }
	}
	
	post{
	success{echo sucsess}
	failure{echo failed}
	}
}
