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
    }
}