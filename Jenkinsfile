/*node {
	stage('Clone repo') {
	sh " echo 'Cloning Repository' "
	checkout scm
	}
	stage('install dependencies') {
		sh "sudo pip install -r requirements.txt"
	}
	stage('deploy app') {
		sh "python guess.py"
	}
}*/

pipeline {
    agent none
    stages {
        stage('Back-end') {
            agent {
                docker { image 'maven:3-alpine' }
            }
            steps {
                sh 'mvn --version'
            }
        }
        stage('Front-end') {
            agent {
                docker { image 'node:7-alpine' }
            }
            steps {
                sh 'node --version'
            }
        }
    }
}