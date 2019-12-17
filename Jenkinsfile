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
                    return my_func(false, false)
                }
            }
            steps {
                sh 'echo expression worked'
            }
        }
    }
}

def my_func(condition1, condition2) {
    println "conditions:"
    println condition1
    println condition2
    return condition1 || condition2
}
