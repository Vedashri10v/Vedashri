pipeline {
    agent any

    stages {

        stage('Plan phase') {
            steps {
                echo 'Hi. This is Vedashri Choudhary'
            }
        }

        stage('code phase') {
            steps {
                input('Do you want to continue?')
            }
        }

        stage('integrate phase') {
            when {
                not {
                    branch "master"
                }
            }
            steps {
                echo 'Integration test passed'
            }
        }

        stage('testing phase') {
            parallel {

                stage('unit test') {
                    steps {
                        echo 'running unit test'
                    }
                }

            }
        }

    }
}
