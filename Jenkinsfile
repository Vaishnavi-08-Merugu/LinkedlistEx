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
        stage('Build and Run')
        {
            steps
            {
                echo 'Building and Running Java Program...'
                javac LinkedList.java
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