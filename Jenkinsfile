pipeline{
    agent any
    stages{
        stage(Buiild){
            steps{
                sh 'mvn -version'
                sh 'mvn package'
                sh 'docker build --platform linux/amd64 -t spring-helloworld:$BUILD_ID .'
                sh 'docker tag akshaydevops08/spring-demo:$BUILD_ID'
                withDockerRegistry(credentialsId: 'Dockerhub1', url: 'https://hub.docker.com/') {
                    dockerImage.push()
                }
            }
        }
    }
}