pipeline {
    agent any

    environment {
        // Define environment variables if needed
        NODE_HOME = 'C:/Program Files/nodejs' // Update the path to where Node.js is installed
        PATH = "${NODE_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Install Dependencies') {
            steps {
                script {
                    // Install dependencies (e.g., npm install for Node.js projects)
                    bat 'npm install'
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    // Run your test script (can be mocked for now)
                    // Example: running a test script or a sample test
                    bat 'npm test'  // Replace with your actual test command
                }
            }
        }

        stage('Archive Artifacts') {
            steps {
                script {
                    // Archive the test results or any files generated during the build
                    //archiveArtifacts '**/test-*.log'  // Adjust the path based on your files
                }
            }
        }
    }

    post {
        always {
            // Clean up or send notifications (if required)
            echo 'Cleaning up...'
        }
    }
}
