pipeline {
   agent any
   tools {
      maven 'Maven'
   }
   stages {
       stage("build") {
                steps {
                    snDevOpsStep ()
                    echo "Building" 
                    sh 'mvn -X clean install -DskipTests'
                    sleep 5
                }
       }
  
       stage("deploy") {
           steps {
               snDevOpsStep ()
               snDevOpsChange()
               echo "Deploying"
               // release process
              
               sleep 7
           }
       }
  }
}
