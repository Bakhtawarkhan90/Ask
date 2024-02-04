pipeline{
    agent any
    stages{
        stage ("Fetching Code"){
            steps{
                git url:"https://github.com/Bakhtawarkhan90/Ask-Her.git", branch: "main"
            }
        }
        stage ("Building image"){
            steps{
                sh "docker build . -t ask-her"
            }
        }
        stage ("Running the conatiner"){
            steps{
                sh "docker-compose down -d"
                sh "docker-compose up -d"
            }
        }
    }
}
