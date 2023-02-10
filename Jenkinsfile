pipeline {
   agent any
   
   environment {
      gitBranch = scm.branches[0].toString().replace('*/','')
   }
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
      stage('env') {
         steps {
            script {
               sh 'echo "Hello from Build 3"'
               echo /*"${evn.gitBranch} on */ "${BUILD_NUMBER}"
            }   
         }
      }
   }
}
