# Hello-World
Hello world
pipeline{
    agent any
stages{
    stage('Build'){
        steps {
        git credentialsId: 'git-cred', url: 'https://github.com/ehtasham-azhar/Hello-World'
        sh 'mvn -f Code\\pom.xml install -DskipTests'
        sh 'java -jar Code\\target\\journals-1.0.jar'
        }
}

}

}