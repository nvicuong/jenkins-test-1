pipeline {
    agent none
    environment {
      hello = 'echo "hello alohaaaa"'
      goodbye = 'echo "good bye"'
    }
    stages {
        stage('build') {
            agent {
               label 'agent-1'
            }
            steps {
                sh(script: """ ${hello} """, label: "print hello")
            }
        }
        stage('deploy') {
            agent {
              label 'agent-2'
            }
            steps {
                sh(script: """ ${goodbye} """, label: "print goodbye")
            }
        }
    }
}

