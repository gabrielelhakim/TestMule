pipeline {
  agent any
  stages {
    stage('Unit Test') { 
      steps {
         mvn clean test
      }
    }
    stage('Deploy Standalone') { 
      steps {
         mvn deploy -P standalone
      }
    }
    stage('Deploy Cloudhub DEV') { 
      steps {
         mvn deploy -DmuleDeploy -Dcloud.env=DEV -DcloudhubAppName=api-template-dev -Dmule.version=4.2.0 -Dcloud.user=gabriel_elhakim -Dcloud.password=Mikgabyah_123    	
      }
    }
  }
}