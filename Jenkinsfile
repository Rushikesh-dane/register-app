Pipeline{
    agent{label 'Jenkins-agent'}
    tools{
        jdk 'Java17'
        maven 'Maven3'
    }
    stages{
        satge("Cleanup Wokspace"){
            steps{
                cleanws()
            }
        }

        stage("Checkotut from SCM"){
            steps{
                git branch: 'Main', credentialsId: 'github', url: 'https://github.com/Rushikesh-dane/register-app'
            }


        }

        stage("Build Application"){
            steps{
                sh 'mvn cleanup package'
            }
        }

        stage("Test Application"){
            steps{
                sh "mvn test"
            }
        }

    }
}
