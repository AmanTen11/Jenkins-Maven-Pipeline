pipeline {
    agent {label 'WindowsSlave'}

    stages {
        stage ('Compile Stage') {

            steps {			
                bat 'mvn clean'
            }
        }        
    }
}