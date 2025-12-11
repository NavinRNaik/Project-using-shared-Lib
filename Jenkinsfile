@Library('my-shared-lib') _

pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Maven Build') {
            steps {
                mavenBuild()
            }
        }

        stage('Docker Build') {
            steps {
                script {
                    dockerBuild("my-maven-app:latest")
                }
            }
        }
    }

    post {
        always {
            echo "Pipeline Finished."
        }
    }
}
