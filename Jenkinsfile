pipeline {
    agent { 
       node {
         label "testarea" 
         customWorkspace "R:/IT/DEVOPS/DEVOPSCLS/JENKINSCLS/SLAVE/workspace/demo"
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
                build quietPeriod: 4, job: 'sample project'
            }
        }
    }
}
