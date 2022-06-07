pipeline{
    agent any
    stages{
        stage ('Compile stage'){
            steps {
                withMaven( maven : "maven_3.8.5"){
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing stage'){
            steps{
                withMaven( maven : 'maven_3.8.5'){
                    sh 'mvn test'
                }
            }
        }

        stage ('Build stage'){
            steps{
                withMaven(maven : 'maven_3.8.5'){
                    sh 'mvn package'
                }
            }
        }
    }
}