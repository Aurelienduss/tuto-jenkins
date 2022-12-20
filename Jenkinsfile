pipeline {
    agent any

    stages {
        stage('Verify Branch') {
            steps {
                echo "oui"
            }
        stage('Docker buid'){
            steps {
                pwsh(script:'docker images -a')
                pwsh(script: """
                cd azur-vote/
                docker images -adocker build -t jenkins-pipeline .
                docker images -a
                cd ..
                """)
               
            }
        }
    }
}
