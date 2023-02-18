pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG20CS403-1 working-pipeline.cpp'
                print "Build Successful"
            }
        }
        stage('Test') {
            steps {
                ssh './PES2UG20CS403-1'
            }
        }
    }
    post {
        always {
            echo 'Pipeline completed'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
