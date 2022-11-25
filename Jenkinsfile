pipeline{
    agent any 
    environment {
        ENV_URL = "pipeline.google.com"
    }
    options {
        disableConcurrentBuilds()
        timeout(time: 1, unit: 'MINUTES')
    }
    stages{
        stage("Hello Worls"){
            steps{
                sh "echo Hello World1"
                sh "sleep 1000"
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