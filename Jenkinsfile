pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Building file and creating the jar file"
                sh 'tar zcvf TopicProject.tar.gz TopicProject'
            }
        }
        stage('Deploy') {
            steps {
                echo "Jar file is deployed"
            }
        }
    }
    post{
        always{
            echo "This will always run"
        }
        success{
            echo "This will run on success"
        }
        failure{
            echo "This will run on failur"
        }
        unstable{
            echo "This will run only when the run will be marked as unstable"
        }
        changed{
            echo "This will run only when the stage of the pipeline will change"
        }
    }
}
