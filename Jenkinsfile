pipeline {
    agent { 
	docker { 
	  image 'python:3.13.5-alpine3.22'
	  label 'docker'
	} 
    }
    stages {
        stage('version') {
            steps {
                sh 'python --version'
            }
        }
	stage('Parallel Stage') {
	parallel {
	   stage('date 1') {
             steps {
                sh 'date; sleep 10'
             }
           }
	   stage('date 2') {
             steps {
                sh 'date; sleep 10'
             }
           }
	   stage('date 3') {
             steps {
                sh 'date; sleep 10'
             }
           }
	}}
    }
}
