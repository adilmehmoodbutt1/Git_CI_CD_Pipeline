pipeline {
    //agent {
        //docker {
          //  image 'node:6-alpine'
            //args '-p 3000:3000'
      //  }
  //  }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                echo 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo './jenkins/scripts/test.sh'
            }
        }
        stage('Deliver') {
            steps {
                echo './jenkins/scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                echo './jenkins/scripts/kill.sh'
            }
        }
    }
}
