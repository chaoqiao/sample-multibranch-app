pipeline { 
    agent any
    options {
        disableConcurrentBuilds()
    }

    stages{
        stage('hello'){
            steps{
                echo "Hello"
            }
        }
        stage('dev'){
            when { branch 'dev'}
            steps{
                sh "cat README.md"
            }
        }
        stage('PR'){
            when { branch 'PR-*'}
            steps{
                echo "This is PR branch"
            }
        }
    }
}