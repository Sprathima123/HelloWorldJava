pipeline {
    agent any

    stages {
        // Stage 1: Triggers only on Pull Requests
        stage('PR Triggered Stage') {
            when {
                changeRequest()
            }
            steps {
                echo 'Running stage for Pull Request creation/update...'
                // Add your PR build, test, or linting steps here
            }
        }

        // Stage 2: Triggers ONLY on direct commits to the main branch
        stage('Main Branch Commit Stage') {
            when {
                    branch 'main'
                    branch 'DEV'
                }
            steps {
                echo 'Running stage for direct commit to main branch...'
                // Add your deployment or main build steps here
            }
        }
    }
}
