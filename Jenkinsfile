node {
        stage('Preparation') {
            catchError(buildResult: 'SUCCESS') {
                sh 'docker stop samplerunning'
                sh 'docker rm samplerunning'
            }
        }
// }
        stage('Build') {
            build 'SampleAppStart'
        }
        stage('Results') {
            build 'TestSampleApp'
        }
    }