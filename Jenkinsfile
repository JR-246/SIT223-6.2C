pipeline{
    stages{
        stage('Build'){
            steps{
                echo "Build the code using a build automation tool to compile and package the code"
                echo "Example: Maven"
            }
        }
        stage('Unit and Integration Tests'){
            steps{
                echo "Run unit tests to ensure the code functions as expected and run intergration tests to ensure the different components work together"
                echo "Example: Citrus"
                echo "Sending email ..."
            }
            post{
                success{
                    mail to: "06bluebird06@gmail.com",
                    subject: "Build Status Email",
                    body: "Unit and Integration Tests was successful"
                }
            }
        }
        stage('Code Analysis'){
            steps{
                echo "Integrate a code analysis too to analyse the code and ensure it meets the standards"
                echo "Example: SonarQube"
            }
        }
        stages('Security Scan'){
            steps{
                echo "Perform a secuirty scan on the code"
                echo "Example: Jenkins Security Scan"
                echo "Sending email ..."
            }
            post{
                success{
                    mail to: "06bluebird06@gmail.com",
                    subject: "Build Status Email",
                    body: "Security Scan was successful"
                }
            }
        }
        stages('Deploy to Staging'){
            steps{
                echo "Deploy the application to a staging server"
                echo "Example: AWS EC2 Instane"
            }
        }
        stages('Integration Tests on Staging'){
            steps{
                echo "Run intergration tests on the staging environment"
                echo "Example: Citrus"
                echo "Sending email ..."
            }
            post{
                success{
                    mail to: "06bluebird06@gmail.com",
                    subject: "Build Status Email",
                    body: "Intergration Tests on Staging was successful"
                }
            }
        }
        stages('Deploy to Production'){
            steps{
                echo "Deploy the application to a production server"
                echo "Example: AWS EC2 Instance"
            }
        }
    }
}