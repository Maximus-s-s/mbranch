pipeline {
   agent any
   stages {
      stage('Build 1') {
         steps {
            sh 'echo "Hello from Build 1"'
         }
      }
      stage('Build 2') {
         steps {
            sh 'echo "Hello from Build 2"'
         }
      }
      stage('Build 3') {
         steps {
            script {
               echo "${evn.gitBranch}_${BUILD_NUMBER}"
            }   
         }
      }
   }
}
