import groovy.json.JsonSluerClassic

def jsonParse(def json) {
    new groovy.json.JsonSluerClassic().parseText(json)
}

pipeline {
    agent {label 'master' }
    environment {
        appName = "vriable"
    }
    stages {
        stage("Step 1") {
            steps {
                script {
                    sh "echo hola mundo"
                }
            }
        }
    }
    post {
            always {
                deleteDir()
                sh "echo 'fase always'"
            }
            success {
                sh "echo 'fase success'"
            }
            failure {
                sh "echo 'fase failure'"
            }
    }
}
