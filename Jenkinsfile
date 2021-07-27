pipeline {
    agent none 
    stages { 
        stage ('Non-Parallel Stage') {
            agent {
                   label "master"
            }
            steps { 
                echo "This stage will be executed first";
            }
        }
    
        stage('Run Tests') {
            parallel {
                stage ('Tests on Windows'){
                    agent {
                        label 'Windows_Node'
                    }
                    steps{
                        echo "Task 1 on Agent"
                    }
                }
                stage ('Tests on Master'){
                    agent {
                        label 'master'
                    }
                    steps{
                        echo "Task 1 on Master"
                    }
                }
                
            }
        }
}
}
        
    

           
