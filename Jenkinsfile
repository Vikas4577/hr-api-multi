pipeline{
    agent any
    stages{
        stage("Git Checkout"){
            steps{
                git url:"https://github.com/Vikas4577/hr-api-multi", branch: "main"
            }
        }
        stage("Maven Build"){
            steps{
                sh "mvn clean package"
            }
        }
        stage("Dev Deploy"){
            when{
                branch'devlop'
            }
            steps{
                echo "deploying to dev environment"
            }
        }
        stage("QA Deploy"){
            when{
                branch'qa'
            }
            steps{
                echo "deploying to qa environment"
            }
        }
        stage("UAT Deploy"){
            when{
                branch'uat'
            }
            steps{
                echo "deploying to uat environment"
            }
        }
        stage("Prod Deploy"){
            when{
                branch'maim'
            }
            steps{
                echo "deploying to production environment"
            }
        }
    }
}