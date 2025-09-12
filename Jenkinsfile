
pipeline {
    agent any

    stages {
        stage("Test") {
            steps {
                script {
                    echo "Testing application ..."
                    echo "Executing pipeline for $BRANCH_NAME"
                }
            }

        }
        stage("Build") {
            when {
                expression {
                    BRANCH_NAME == "main"
                }
            }
            steps {
                script {
                    echo "Building application ..."
                }
            }

        }
        stage("Deploy") {
            when {
                expression {
                    BRANCH_NAME == "main"
                }
            }
            steps {
                script {
                    echo "Deploying application ..."
                
                }
            }

            post {
                success {
                    echo "Build sucess in $BRANCH_NAME"
                }
            }

        }
    }
}