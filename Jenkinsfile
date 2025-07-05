pipeline {
    agent { label 'genesis-agent' }

    stages {
        stage('Dynamic Parallel Tasks') {
            steps {
                script {
                    // Simulate fetching data from an API
                    def services = ['auth-service', 'payment-service', 'user-service']
                    def parallelStages = [:]

                    for (int i = 0; i < services.size(); i++) {
                        def serviceName = services[i]

                        parallelStages[serviceName] = {
                            stage("Run for ${serviceName}") {
                                echo "Processing ${serviceName}"
                                sh """
                                    echo "Deploying ${serviceName}"
                                    sleep 2
                                """
                            }
                        }
                    }

                    parallel parallelStages
                }
            }
        }

        stage('Done') {
            steps {
                echo 'All parallel tasks complete.'
            }
        }
    }
}
