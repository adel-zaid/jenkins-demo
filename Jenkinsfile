pipeline {
    agent any
    tools {
        gradle '8.3'
    }

    stages {
        stage ('Pull changes') {
            steps {
                git branch: 'main', url: 'https://github.com/adel-zaid/jenkins-demo'
            }
        }
        stage ('Build') {
            steps {
                sh "./gradlew clean build"
            }
        }
    }
}
