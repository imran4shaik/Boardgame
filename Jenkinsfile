pipeline {
    agent {label 'agent-1'}

    tools {
        jdk 'jdk17'    
    }
    
    stages {
        stage('Git Checkout') {
            steps {
               git branch: 'main', url: 'https://github.com/imran4shaik/Boardgame.git'
            }
        }
        
         stage('Compile') {
            steps {
              sh 'mvn compile'      // Jenkins doesn't understand mvn. so we want it to execut as shell command....
            }
        }
        
         stage('Test') {
            steps {
               sh 'mvn test'
            }
        }
        
         stage('Build') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
