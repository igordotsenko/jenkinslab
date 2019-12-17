pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
                sh 'echo hello'
            }
        }
        stage('test_expression') {
            when {
                expression {
                    return true
                }
            }
        }
        steps {
            sh 'echo expression worked'
        }
    }
}
