pipeline {
    agent {
        label 'agent1'
    }
    options {
        // keep the 5 most recent builds
        buildDiscarder(logRotator(numToKeepStr: '5'))
    }
    environment {
        TOOL_USED = 'Jenkins'
    }
    stages {
        stage('Stage 1') {
            steps {
                echo "This is my first ${TOOL_USED} tutorial!"
                echo "This tutorial is running ${env.BUILD_ID} on ${env.JENKINS_URL} with current build number ${env.BUILD_NUMBER}"
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}