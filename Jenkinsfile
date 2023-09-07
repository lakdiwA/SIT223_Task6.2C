pipeline {
    agent any
    stages{
        stage('Build') {
            steps{
                echo "The code is built using the automation tool Maven"
            }
        }
        stage('Unit and Integration Tests') {
            steps{
                echo "Unit tests are done by automated tool JUnit"
            }
            post{
                success{
                    emailext to: "ranujalakdive@gmail.com",
                    subject: "Test build success",
                    body: "The test build was a success"
                    attachLog: true
                }
                failure{
                    emailext to: "ranujalakdive@gmail.com",
                    subject: "Test build failure",
                    body: "The test build was a fail"
                }
            }
        }
        stage('Code Analysis') {
            steps{
                echo "To check the quality of the code by automatically analysing the code CheckStyle will be used"
            }
        }
        stage('Security Scan') {
            steps{
                echo "To perform security scans a plugin called OWASP ZAP will be used"
            }
            post{
                success{
                    emailext to: "ranujalakdive@gmail.com",
                    subject: "Security scan-build success",
                    body: "The security scan-build was a success"
                }
                failure{
                    emailext to: "ranujalakdive@gmail.com",
                    subject: "Security scan-build failure",
                    body: "The security scan-build was a fail"
                }
            }
        }
        stage('Deploy to Staging') {
            steps{
                echo "AWS EC2 instance will be used to deploy staging"
            }
        }
        stage('Integration Tests on Staging') {
            steps{
                echo "To do Integration tests on the staging JUnit is used"
            }
        }
        stage('Deploy to Production') {
            steps{
                echo "AWS EC2 instance is used to deploy production"
            }
        }
    }
}
