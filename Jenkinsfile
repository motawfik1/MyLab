pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World" > file1' 
                sh '''
                    echo "Multiline shell steps works too" >> file1
                    ls -lah
                '''
            }
        }
    }
     post {
        always {
            echo 'One way or another, I have finished'
        }
        success {
            echo 'I succeeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            echo 'I failed :('
        }
        changed {
            echo 'Things were different before...'
        }
    }
}
