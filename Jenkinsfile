pipeline {
    agent any
    stages {
        stage("Parallel") {
            parallel {
                stage("First") {
                    steps {
                        sh "sleep 10 && echo 'first done'"
                    }
                }
                stage("Second") {
                    steps {
                        sh "sleep 5 && echo 'second done'"
                    }
                }
                stage("Third") {
                    stages {
                        stage("Third - 1") {
                            steps {
                                sh "sleep 2 && echo '3-1 done'"
                            }
                        }
                        stage("Third - 2") {
                            steps {
                                sh "sleep 2 && echo '3-2 done'"
                            }
                        }
                    }
                }
            }
        }
    }
}
