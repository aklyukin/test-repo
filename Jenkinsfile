pipeline {
    agent any
    triggers { 
        pollSCM('H/2 * * * *') 
    }
    stages {
        stage('build') {
            steps {
                sh 'echo "bla"'
            }
        }
    }
}
