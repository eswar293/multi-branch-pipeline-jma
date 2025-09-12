
pipeline {
    agent any

    stages {
        stage("Test") {
            steps {
                script {
                    echo "Testing application ..."
                    ecgo "Executing pipeline for $BRANCH_NAME"
                }
            }

        }
        stage("Build") {
            steps {
                script {
                    when{
                        expression{
                            BRANCH_NAME == "maiin"
                        }
                    }
                    echo "Building application ..."
                }
            }

        }
        stage("Deploy") {
            steps {
                script {
                    echo "Deploying application ..."
                    when{
                        expression{
                            BRANCH_NAME == "maiin"
                        }
                    }
                }
            }

        }
    }
}