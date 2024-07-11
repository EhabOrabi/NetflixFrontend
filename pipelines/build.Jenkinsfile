// pipelines/build.Jenkinsfile

pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Build app container') {
            steps {
                sh '''
                    # your pipeline commands here....
                    npm run build
                    # for example list the files in the pipeline workdir
                    ls

                    # build an image
                    docker build -t netflix-front .
                    npm start
                '''
            }
        }
    }
}