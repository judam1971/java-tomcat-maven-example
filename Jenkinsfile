pipeline {
    agent any
    stages {
        stage ('Build Servlet Project') {
            steps {
                /*For windows machine */
                  bat 'C:\\'Program Files'\\apache-maven-3.6.1\\bin\\mvn clean package'
                  
 
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
