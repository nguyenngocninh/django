pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                dir("${WORKSPACE}") {
                    // Now you are inside the workspace directory
                    sh 'ls' // Print the current directory (workspace)

                    // You can perform other actions inside the workspace directory here
                }
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
                    sh 'ls'
                    sh 'docker run  -p 3000:3000 -v ./frontend:/frontend  demo_djago_main_web:latest'
                    
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

