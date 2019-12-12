pipeline {
   agent any

   tools {
      // Install the Maven version configured as "M3" and add it to the path.
      maven "maven 3.6.1"
   }

   stages {
      stage('git') {
         steps {
            // Get some code from a GitHub repository
            git 'https://github.com/Abbes07/git_maven.git'
         }
          }
      
      stage('maven') {
         steps {          
          // Run Maven on a Unix agent.
            sh "mvn clean package"
         }
      }
      stage('execute') {
         steps {          
          // Run Maven on a Unix agent.
            sh "java -jar target/git-1.0-SNAPSHOT.jar"
         }
      }      
            // To run Maven on a Windows agent, use
            // bat "mvn -Dmaven.test.failure.ignore=true clean package"
         
      
   }
}
