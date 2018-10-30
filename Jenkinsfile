pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    bat 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    bat 'mvn test'
                }
            }
        }


        stage ('SonarQube Stage') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    bat 'mvn sonar:sonar'
                }
            }
        }
    }
}