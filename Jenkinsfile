pipeline {
        agent any

        stages {
                stage('Build') {
                        steps {
                            build 'PES2UG21CS172-1'
                            echo 'building'
                            
                                sh 'g++ -o myprogram main/hello.cpp'
                        }
                }

                stage('Test') {
                        steps {
                                sh './myprogram'
                        }
                }
            stage('Deploy'){
                steps{
                    echo 'Deploying'
                        sh 'deploy'
                }
            }
        }
post{
    failure{
        echo 'pipline failed'
    }
}
}
