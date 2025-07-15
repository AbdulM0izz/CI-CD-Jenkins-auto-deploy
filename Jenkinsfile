pipeline{
    agent any
    environment {
        vercelToken = credentials('vercel-token')
    }
    stages{
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

         stage('Test') {
            steps {
                echo 'Running steps'
            }
        }

         stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

         stage('Deploy') {
            steps {
                sh 'npx vercel --prod --yes --token=$VERCEL_TOKEN'
            }
        } 
    }
}