pipeline {
agent any
     tools {
        maven 'localMaven'
    }
    stages {
        stage('Build') {
            steps {
                 sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                    mvn clean
                '''
            }
        }
        stage('Deliver') {
                    steps {
                        sh './jenkins/scripts/deliver.sh'
                    }
                }
    }
}
