pipeline {
    agent any

    stages {
        stage("Code Build") {
            steps {
                dockerbuild("notes-app", "latest")
            }
        }
        stage("Push to DockerHub") {
            steps {
                dockerpush("dockerHubCreds", "notes-app", "latest")
            }
        }
        stage("Deploy") {
            steps {
                deploy()
            }
        }
    }
}
