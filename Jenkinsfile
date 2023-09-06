pipeline {
    agent any
    environment{
        DIRECTORY_PATH= "https://github.com/hirushanirmalt/Deakin-Unit-Page";
        TESTING_ENVIRONMENT= "Testing Environment";
        PRODUCTION_ENVIRONMENT= "Ranuja Aththidiya";
    }
    stages{
        stage('Build') {
            steps{
                echo "fetch the source code from the directory path specified by the environment variable"
            }
        }
        stage('Test') {
            steps{
                echo "unit tests"
                echo "integration tests"
            }
        }
        stage('Code Quality Check') {
            steps{
                echo "check the quality of the code"
            }
        }
        stage('Deploy') {
            steps{
                echo "deploy the application to a testing environment specified by the environment variable"
            }
        }
        stage('Approval') {
            steps{
                sleep 10
            }
        }
        stage('Deploy to Production') {
            steps{
                echo "The code is deployed to %PRODUCTION_ENVIRONMENT%"
            }
        }
        stage('stage 7') {
            steps{
                echo "This is stage 7"
            }
        }
    }
}
