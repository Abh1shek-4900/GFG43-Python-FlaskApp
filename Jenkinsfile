pipeline { //pipeline
    agent {label "runners" }
    stages { //collection of stages
        stage("Deploy the app in dev env"){ // job1
            steps {
                sh 'docker pull abhidocker4900/pythonflaskcicd:latest'
                sh 'docker rm -f webapp'
                sh 'docker run -dit --name webapp -p 80:80 abhidocker4900/pythonflaskcicd:latest'
            }
        }
    }
}