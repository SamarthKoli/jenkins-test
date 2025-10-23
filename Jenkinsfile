pipeline{

    agent any
    options{
       skipStagesAfterUnstable()

    }
    stages{
        stage('Build'){
            steps{
                sh 'mvn -B -DskipTests clean package'
            }
        }

        stage('Test'){
            steps{
                sh 'mvn test'
            }
            post {
                echo 'Testing succesfully done'
            }
        }
    }

}