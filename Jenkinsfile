pipeline {
        agent any
        stages {
        stage('First') {
                steps {
                echo  env.execute="True"
                }
        }
        stage('Second'){
                steps{
                 sh 'echo "Updating Second Stage"'
                }

                 when {
                        environment name: 'execute',
                        value:'True'
            }
        }
         stage('Three') {
            steps {
                sh 'echo "Step Three"'
            }
                when {
                        environment name: 'execute',
                        value:'False'
            }
        }
     }		
}
