pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Compile the .cpp file using a shell script
                sh 'ls'
                build 'PES2UG21CS455-1'
                sh 'g++ -o obj main/hello.cpp'
            }
        }

        stage('Test') {
            steps {
                // Print the output of the compiled .cpp file
                sh './obj'
            }
        }

        stage('Deploy') {
            steps {
              ech 'deploy'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
