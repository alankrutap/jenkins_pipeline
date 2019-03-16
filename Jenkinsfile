pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Loca_Maven') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'Loca_Maven') {
                    sh 'mvn test'
                }
            }
        }
        stage ('Verifying Stage') {

            steps {
                withMaven(maven : 'Loca_Maven') {
                    sh 'mvn verify'
                }
            }
        }

        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'Loca_Maven') {
                    sh 'mvn install'
                }
            }
        }
    }
}
