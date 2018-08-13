pipeline {
agent any
     tools {
        maven 'Maven 3.5.3'
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
