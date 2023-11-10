pipeline {
    agents any
    tools {
        tool name: 'gradle', type: 'gradle'
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