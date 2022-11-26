pipeline{
    agent any 
    triggers { pollSCM('*/2 * * * *') }
    environment {
        ENV_URL = "pipeline.google.com"
    }
    options {
        disableConcurrentBuilds()
        timeout(time: 1, unit: 'MINUTES')
    }
    tools {
            maven 'maven-3.5.0'
    }
    stages{
        stage("Hello Worls"){
            steps{
                sh "echo Hello World1"
                
            }       
                  
        }
        stage("Hello World1"){
            steps{
                sh "echo Hello World"
                sh "echo ENV_URL is ${ENV_URL}"
            }
        }
        stage("Hello World2"){
            environment {
                ENV_URL = "stage.krishan.com"
            }
            steps{
                sh "echo Hello World"
                sh "echo ENV_URL is ${ENV_URL}"

}
        }
    }
}