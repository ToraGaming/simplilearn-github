pipeline {
    agent any
    
    stages {
        stage('Git-Checkout') {
            steps {
                echo "Checking out from Git Repo";
            }
        }
        stage('Build') {
            steps {
                echo "Building the checked-out project!";
            }
        }
        stage('Unit-Test') {
            steps {
                echo "Running JUnit Tests";
            }
        }
        stage('Quality-Gate') {
            steps {
                echo "Verifying Quality Gates";
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying to Stage Environment for more tests!";
            }
        }
    }
    
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
