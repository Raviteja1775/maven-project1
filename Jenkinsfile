pipeline {
    agent { 
       node {
         label "testarea" 
         customWorkspace "R:/IT/DEVOPS/DEVOPSCLS/JENKINSCLS/SLAVE/workspace/pipeline2"
       }
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Test') {
            steps {
                echo 'Hello Test stage'
            }
        }
        stage('Prod') {
            steps {
                echo 'Hello Prod stage'
                build quietPeriod: 4, job: 'pipeline1'
            }
        }
    }
}
