pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                dir("${WORKSPACE}") {
                    // Now you are inside the workspace directory
                    sh 'pwd' // Print the current directory (workspace)
                    
                    // You can perform other actions inside the workspace directory here
                }
            }
        }
        //stage("ssh-server") {
        //    steps {
       //         sshagent(['ssh-remote']) {
        //            sh 'ssh root@localhost -o StrictHostKeyChecking=no -p 2022 '
       //         }
       //     }
      //  }
    }
}

