pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    eccho 'Compiling the C++ file...'
                    sh "g++ -o PES2UG21CS302-1 PES2UG21CS302.cpp"
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running the C++ program...'
                    sh "./PES2UG21CS302-1"
                }
            }
        }

        stage('Deploy') {
            steps {
                 echo 'Deployment stage'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
