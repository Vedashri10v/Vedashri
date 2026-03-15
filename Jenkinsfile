pipeline {
    agent any

    stages {

        stage('Plan phase') {
            steps {
                echo 'Hi. This is Vedashri Choudhary'
            }
        }

        stage('Code phase') {
            steps {
                input 'Do you want to continue?'
            }
        }

        stage('Security Check') {
            steps {
                echo 'Run the security check against the application'
            }
        }

        stage('Integrate phase') {
            when {
                not {
                    branch 'master'
                }
            }
            steps {
                echo 'Integrating code changes'
            }
        }

        stage('Testing phase') {
            parallel {

                stage('Unit Test') {
                    steps {
                        echo 'Running unit test'
                    }
                }

                stage('Integration Test') {
                    steps {
                        echo 'Integration test passed'
                    }
                }

            }
        }

        stage('Publish Artifacts') {
            steps {
                echo 'Save the assemblies generated from the compilation'
            }
        }

    }
}
