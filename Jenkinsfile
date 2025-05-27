pipeline {
    agent any
    stages {
        stage('Run test1') {
            steps {
                script {
                    def result1 = build job: 'test1', propagate: true
                    echo "test1 completed successfully."
                }
            }
        }
        stage('Run test2') {
            steps {
                script {
                    def result2 = build job: 'test2', propagate: true
                    echo "test2 completed successfully."
                }
            }
        }
        stage('Run test3') {
            steps {
                script {
                    def result3 = build job: 'test3', propagate: true
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
            echo "All tests executed successfully."
        }
    }
}
