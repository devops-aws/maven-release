#!/usr/bin/env groovy

pipeline {
    agent any
    options {
        timestamps()
    }
    stages {
        stage('clean') {
            steps {
                echo("Building project for me")
                sleep(time:5,unit:'SECONDS')
		            sh 'mvn clean'
            }
            post {
                success {
                    echo("Clean stage completed with result 'SUCCESS'.")
                }
                failure {
                    echo("Clean stage completed with result 'FAILURE'.")
                }
            }
        }
        stage('package') {
            steps {
                echo("Testing project for me")
                sleep(time:5,unit:'SECONDS')
		            sh 'mvn package'
            }
            post {
                success {
                    echo("package stage completed with result 'SUCCESS'.")
                }
                failure {
                    echo("package stage completed with result 'FAILURE'.")
                }
            }
        }
    }
    post {
        success {
            echo("Pipeline completed for me with result 'SUCCESS'.")
        }
        failure {
            echo("Pipeline completed for me with result 'FAILURE'.")
        }
    }
}
