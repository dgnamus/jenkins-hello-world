pipeline {
    agent any

    tools {
        // Install the Maven version and add it to the path
        maven "M398"
    }

    stages {
        stage('Echo Version') {
            steps {
                sh 'echo Print Maven Version'
                sh 'mvn -version'
            }
        }
        
        stage('Build') {
            steps {
                // Get some code from GitHub repo
                // git branch: 'main', url: 'https://github.com/dgnamus/jenkins-hello-world.git'
                
                // Run Maven Package CMD
                sh 'mvn clean package -DskipTests=true'
            }
        }
        
        stage('Unit Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
