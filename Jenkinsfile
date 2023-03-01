pipeline {
    agent any
    triggers {
        cron('* * * * *)
    }
    stages {
        stage('Run shell command') {
            steps {
                sh 'echo "hello, world! >> test"'
            }
        }
 
        stage('Commit and push changes') {
            steps {
                sh 'git add test'
                sh 'git commit -m "Update Refresh Token By Jenkins"'
                sh 'git push origin master'
            }
        }
    }
}
