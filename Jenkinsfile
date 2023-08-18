pipeline {
    agent any 
    stages{ 
    stage (' Init '){
        steps {
          sh  "rm docker rm -f $(docker ps -aq)"
        }
    }
    stage (' Build '){
        steps {
            sh "docker build . -t app_image"
        }
    }
    stage (' Deploy '){
        steps {
            sh "docker run -d -p  80:5500 --name appy  app_image"
        }
   }
 }
}