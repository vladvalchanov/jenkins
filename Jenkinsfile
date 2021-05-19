 pipeline {
    agent any
    
    stages {
     
       stage("Build") {
            steps {
                sh "date"
            }
        }
        stage("Ok") {
            steps {
                echo "Ok"
            }
        }
    
    }
    post {
     always {
            emailext body: 'A Test EMail', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Test'
            cleanWs() 
        }
    }
}
