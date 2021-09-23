pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(localMVN : 'maven_3_5_0') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(localMVN : 'maven_3_5_0') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(localMVN : 'maven_3_5_0') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
