pipeline {
    agent any
    stages {
        stage ('Build Servlet Project') {
            steps {
                /*For windows machine */
                  //bat 'mvn clean package'
                  bat 'echo %M2_HOME%'
 
                /*For Mac & Linux machine */
               // sh  'mvn clean package'
            }
 
            post{
                success{
                    echo 'Now Archiving ....'
 
                    archiveArtifacts artifacts : '**/*.war'
                }
            }
        }
    }
}
