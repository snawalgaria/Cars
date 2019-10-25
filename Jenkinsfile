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
        environment {
    registry = "https://index.docker.io/v1/"
    registryCredential = 'docker_cred_1'
  }
    agent none
    stages {
        stage('Back-end') {
            agent {
                docker { image 'cnn-tensorflow:latest' }
            }
            steps {
                sh 'mvn --version'
            }
        }
        /*stage('Front-end') {
            agent {
                docker { image 'node:7-alpine' }
            }
            steps {
                sh 'node --version'
            }
        }*/
    }
}
