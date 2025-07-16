pipeline {
    agent any
    stages {
        stage('Cloning Github repo to Jenkins') {
            steps {
                script {
                    echo 'Cloning Github repo to Jenkins'
                    checkout([
                        $class: 'GitSCM',
                        branches: [[name: '*/main']],
                        userRemoteConfigs: [[
                            url: 'https://github.com/LeonardoPatrickI/MLProject1.git',
                            credentialsId: 'github-token'
                        ]],
                        extensions: []
                    ])
                }
            }
        }
    }
}

