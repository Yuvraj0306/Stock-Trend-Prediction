pipeline {
    agent any

    stages {
        stage('run frontend') {
            steps {
                echo 'executing yarn....'
                nodejs('Node-24.08') {
                    sh 'yarn install'
                }
            }
        }
        stage('run backend') {
            tools {
                gradle 'Gradle'
            }
            steps {
                echo 'executing gradle...'
                sh 'gradle -v'
            }
        }
    }
}
