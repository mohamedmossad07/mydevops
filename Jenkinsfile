pipeline{
    agent any
    tools {
        maven "maven"
    }
    stages{
        stage("Initialization Stage"){
            steps{
                echo "========Initialization stage========"
                echo "========Make surring Maven exists========"
                sh "mvn --version"
                echo "========Getting project's source code from SCM========"
                git branch: 'main', url: 'https://github.com/mohamedmossad07/mydevops.git'
                echo "========Priniting working directory========"
                sh "pwd"
                sh "tree ."
            }
            post{
                success{
                    echo "========Build executed successfully========"
                }
                failure{
                    echo "========Build execution failed========"
                }
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}