pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "Esto es el build"
                echo "agrego otra linea"
            }
        }
        stage('Scan') { 
            steps {
                withSonarQubeEnv('SonarQubeScanner4.7'){
                    sh 'mvn sonar:sonar' 
                }
            }
        }
        stage('Test') { 
            steps {
                echo "Este es el test"
            }
        }
        stage('Deploy') { 
            steps {
                echo "Este es el deploy"
            }
        }
    }
}
