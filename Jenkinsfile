pipeline{
    agent{label "dev"}
    stages{
        stage("code"){
            steps{
                git url: "https://github.com/sahastra16/Springboot-BankApp.git", branch: "prd"
            }
        }
        stage("build"){
            steps{
                sh "docker build -t bankapp ."
            }
        }
        stage("deploy"){
            steps{
                sh "docker compose down && docker compose up -d"
            }
        }
    }
}
