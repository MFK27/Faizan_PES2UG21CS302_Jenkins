pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Compiling the C++ file...'
                    sh "g++ -o PES2UG21CS302-1 PES2UG21CS302.cpp"
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running the C++ program...'
                    // Introduce an error by using the wrong file name
                    sh "./PES2UG21CS302-2"
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
            // Introduce a syntax error by removing the single quotes
            echo Pipeline failed!
        }
    }
}
