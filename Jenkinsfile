pipeline {
    agent {
        node {
            label 'nodejs'
       }
    }
    stages {
        state('Run Tests') {
	    parallel {
                stage('Backend Tests') {
                    steps {
                        sh 'node ./backend/test.js'
                    }
                }
                stage('Frontendd Tests') {
                    steps {
                        sh 'node ./frontend/test.js'
                    }
                }
            }
        }
    }
}
