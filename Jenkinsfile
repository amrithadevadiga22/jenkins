pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                values = [:]
                envDir = sh(returnStdout: true, script: "echo $JOB_NAME").split('/')[-3].trim()
                module = sh(returnStdout: true, script: "echo $JOB_NAME").split('/')[-2].trim()
                jobName = sh(returnStdout: true, script: "echo $JOB_NAME").split('/')[-1].trim()
                currentWs = sh(returnStdout: true, script: 'pwd').trim()
                echo "${currentWs}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
