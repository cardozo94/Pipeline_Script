pipeline{
    agent none
    stages{
        stage('Non-parallel stage'){
            agent{
                label "master"
            }
            steps{
                echo 'This stage will be executed first'
            }
        }
        stage('Run Tests'){
            parallel{
                stage('Test On Mac'){
                    agent{
                        label "Mac_Node"
                    }
                    steps{
                        echo "Task1 on Agent"
                    }
                }
                stage('Test On Master'){
                    agent{
                        label "master"
                    }
                    steps{
                        echo "Taks1 on Master"
                    }
                }
            }
        }
    }
}
