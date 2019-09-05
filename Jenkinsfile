pipeline {
  
        stage('Deliver') {
            steps {
                echo './jenkins/scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                echo './jenkins/scripts/kill.sh'
            }
        }
   }
