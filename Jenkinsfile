pipeline
{
    agent any

    stages
    {
        stage('Checkout')
        {
            steps
            {
                echo 'Checking out source code...'
                checkout scm
            }
        }
        stage('Build')
        {
            steps
            {
                echo 'Building...'
                javac LinkedList.java
            }
        }
        stage('Test')
        {
            steps
            {
                echo 'Testing...'
                java LinkedList
            }
        }
        stage('Artifact')
        {
            steps
            {
                echo 'Creating Artifact...'
                archiveArtifacts artifacts: 'LinkedList.class', fingerprint: true
            }
        }

    }
}