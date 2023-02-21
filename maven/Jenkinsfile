pipeline
{
    agent any
    tools
    {
    maven 'MAVEN_HOME'
    }
     
    stages
    {
     
      stage ('cloning')
      {
          steps
          {
              checkout scmGit(branches: [[name: '*/manish']], extensions: [], userRemoteConfigs: [[credentialsId: '3ec48a4e-2e3e-42b1-ad60-f6cd2dd47364', url: 'https://github.com/imp-ress-ico/sandbox.git']])
          }
         
      }
      stage('building')
      {
          steps
          {
              sh 'mvn clean install'
              sh 'pwd'
              sh 'realpath target/simple.project-0.0.1-SNAPSHOT.jar'
              sh '#java -jar ./target/simple.project-0.0.1-SNAPSHOT.jar'
          }
      }
      
    }
}
