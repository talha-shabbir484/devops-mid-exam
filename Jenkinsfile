pipeline {
    agent any

    environment {
        // Define environment variables if needed
        NODE_HOME = '/usr/local/node'
        PATH = "${NODE_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Install Dependencies') {
            steps {
                script {
                    // Install dependencies (e.g., npm install for Node.js projects)
                    sh 'npm install'
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    // Run your test script (can be mocked for now)
                    // Example: running a test script or a sample test
                    sh 'npm test'  // Replace with your actual test command
                }
            }
        }

        stage('Archive Artifacts') {
            steps {
                script {
                    // Archive the test results or any files generated during the build
                    archiveArtifacts '**/test-*.log'  // Adjust the path based on your files
                }
            }
        }

        stage('Install Dependencies') {
    steps {
        bat 'npm install'
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



