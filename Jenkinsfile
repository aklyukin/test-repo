pipeline {
    agent any
    triggers { 
        pollSCM('H/2 * * * *') 
    }
    stages {
        stage('Checkout app repo') {
            steps {
                checkout([
                    $class: 'GitSCM', 
                    branches: [[name: 'master']],
                    extensions: [[$class: 'RelativeTargetDirectory', relativeTargetDir: 'app']], 
                    userRemoteConfigs: [[
                        url: 'https://github.com/aklyukin/test-lib'
                    ]]
                ])
            }
        }
        stage('build') {
            steps {
                sh 'echo "bla"'
            }
        }
    }
}
