pipeline {
   agent any

   triggers {
        pollSCM "*/5 * * * *"
    }

   stages {

      stage('Build Image') {
         steps {
           sh '''
           docker build -t bourawi/p2m:1.2 .
           '''
         }
      }

      stage('Push Image') {
         steps {
           sh '''
           docker tag bourawi/p2m:1.2  bourawi/p2m:1.2
           docker login -u bourawi -p *********
           docker push bourawi/p2m:1.2
           '''
         }
      }

   }
}
