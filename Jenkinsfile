pipeline {
    agent any
    stages {
        stage('Run test1') {
            steps {
                script {
                    echo "Triggering test1 job..."
                    build job: 'test1', propagate: true
                    echo "test1 completed successfully."
                }
            }
        }
        stage('Run test2') {
            steps {
                script {
                    echo "Triggering test2 job..."
                    build job: 'test2', propagate: true
                    echo "test2 completed successfully."
                }
            }
        }
        stage('Run test3') {
            steps {
                script {
                    echo "Triggering test3 job..."
                    build job: 'test3', propagate: true
                    echo "test3 completed successfully."
                }
            }
        }
    }
    post {
        failure {
            echo "Pipeline failed. One of the test jobs did not complete successfully."
        }
        success {
            echo "All test jobs completed successfully."
        }
    }
}
