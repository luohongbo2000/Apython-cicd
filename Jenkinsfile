pipeline {
    agent any
    stages {
        stage('Git-Checkout') {
			steps {
				echo "获得资源库 ";
				git branch: 'master', url: 'git@github.com:lindafanglizhi/thirddemo.git'
			}
		}
        stage('test') {
            steps {
                echo 'build test'
                bat 'python --version'
                bat 'pip install flask pytest'
                bat 'set pythonpath=src;pytest'
            }
        }
    }
}
