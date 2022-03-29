pipeline { 
    agent any 
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') { 
            steps { 
                bat 'make' 
            }
        }
        stage('Test'){
            steps {
                bat 'make check'
                junit 'reports/**/*.xml' 
            }
        }
        stage('Deploy') {
            steps {
                bat 'make publish'
            }
        }
    }
}
