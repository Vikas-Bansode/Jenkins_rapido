pipeline {
    agent any

    
    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code from GitHub...'

                git branch: 'main',
                    url: 'https://github.com/YOUR_USERNAME/rapido-website.git'
            }
        }

        
        stage('Deploy') {
            steps {
                
                    sh '''
                    echo 'Deploying website to the server...'

                    rm -rf /var/www/html/*
                    cp -r * /var/www/html/    
                    '''
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed. Check the Jenkins console output.'
        }
    }
}
```
