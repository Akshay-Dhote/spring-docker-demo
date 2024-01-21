pipeline{
    agent any
    stages{
        stage(Buiild){
            steps{
                sh 'mvn -version'
                sh 'mvn package'
                sh 'docker build --platform linux/amd64 -t spring-helloworld .'
            }
        }
    }
}