node{
  
    stage('code checkout'){
      
      git credentialsID: 'githubID', url: 'https://github.com/devopsprojects-2019/CloneDemo.git'
     }
    
    stage('Build') {
    withMaven(jdk: 'JDK-1.8', maven: 'maven-3.6.1') {
      sh 'mvn clean compile'
      }
    }
    stage('test'){
    
      withMaven(jdk:'JDK-1.8', maven: 'maven-3.6.1'){
      sh 'mvn test'
      }
     }
    
    stage('package'){
      
      withMaven(jdk: 'JDK-1.8', maven: 'maven-3.6.1'){
      sh 'mvn package'
      }
     }
     
 }
