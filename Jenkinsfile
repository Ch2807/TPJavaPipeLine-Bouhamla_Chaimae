pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                // Compilation du fichier Java
                sh 'javac Main.java'
            }
        }

        stage('Run') {
            steps {
                echo 'Running the application...'
                // Exécution et sauvegarde dans result.txt
                sh 'java Main > result.txt'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the output...'
                // Vérification du fichier généré
                sh 'ls -l result.txt'
                sh 'cat result.txt'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}