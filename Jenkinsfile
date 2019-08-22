pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_6_1') {
                    sh 'mvn clean compile -DdoNotUseMyMavenRepo=true'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_6_1') {
                    sh 'mvn test -DdoNotUseMyMavenRepo=true'
                }
            }
        }
/**

        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_6_1') {
                    sh 'mvn deploy -DdoNotUseMyMavenRepo=true'
                }
            }
        }
*/
    }
}