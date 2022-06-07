pipeline{
    agent any
    stages{
        stage ('Compile stage'){
            steps {
                withMaven( maven : 'maven_3.8.5'){
                    bat 'mvn clean compile'
                }
            }
        }

        stage ('Testing stage'){
            steps{
                withMaven( maven : 'maven_3.8.5'){
                    bat 'mvn test'
                }
            }
        }

        stage ('Build stage'){
            steps{
                withMaven(maven : 'maven_3.8.5'){
                    bat 'mvn package'
                }
            }
        }
    }
}