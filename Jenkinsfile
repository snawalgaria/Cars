node {
	stage('Clone repo') {
	sh " echo 'Cloning Repository' "
	checkout scm
	}
	stage('install dependencies') {
		sh "pip install -r requirements.txt"
	}
	stage('deploy app') {
		sh "python guess.py"
	}
}