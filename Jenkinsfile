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
                withSonarQubeEnv('sonarqube'){
                    sh 'mvn sonar:sonar -Dsonar.login=squ_1dc30ebe4aa0f5344d05949c973f8caa8ecae919' 
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
