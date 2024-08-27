pipeline{
 agent any
  triggers {
  pollSCM '* * * * *'
}
 
 stages{
   stage(checkout){
        steps{
          checkout SCM
             }
        }
    stage(build){
         steps{
           sh 'mvn install'
            }
    stage(Deployment){
         steps{
           sh 'cp target/Fourth.war /home/nikita/Documents/devops/apache-tomcat-9.0.93/webapps'
        }
   }
  }  
 } 
}  
