pipeline {
  agent any
  
  stages {
    stage('build') {
	  steps {	  
	  sh 'ant -f build.xml -v'
	  }
	}
  }
  
  post {
    always {
	  archvieArtifacts artifacts: 'dist/*.jar', fingerprint:  true
	}  
  }
}
