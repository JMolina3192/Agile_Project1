pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/JMolina3192/Agile_Project1.git']]])
            }
        }
	stage('Build'){
	    steps {
	        git 'https://github.com/JMolina3192/Agile_Project1.git'
		sh 'python3 test.py'
		echo 'Job building...'
	    }
	}
    }
}
