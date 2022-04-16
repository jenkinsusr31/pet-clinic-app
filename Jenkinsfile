pipeline {
  agent any
    tools {
            maven 'maven-3'
            jdk 'jdk-11'
    }
    stages {      
        stage('Build maven ') {
            steps {     
                    bat 'mvn  clean install package'
            }
        }
        
        stage('Copy Artifact') {
           steps { 
		            bat 'copy -rf target/*.jar docker'
           }
        }
    }
}        
