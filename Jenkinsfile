@Library('jenkins-shared-library@main') _

pipeline {
    agent any
    //options {
        // Timeout counter starts AFTER agent is allocated
        //timeout(time: 1, unit: 'SECONDS')
    //}
    stages {
        stage('Checkout') {
            steps {
                script {
                    log.info 'Downloading repository'
                }
            }
        }
        stage('Building pipelines') {
            steps {
                script {
                    log.info 'Building pipelines...'
                    jobDsl targets: "dsl-jobs/"
                }
            }
        }
    }
}
