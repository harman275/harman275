pipeline{
    agent any
    stages{
        stage("AWS Demo"){
            steps{
                withCredentials([[
                    $class: 'AmazonWebServicesCredentialsBinding',
                    credentialsId: 'jenkins-demo',
                    accessKeyVariable: 'AWS_ACCESS_KEY_ID',
                    secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
                        
                        sh 'aws ec2 describe-instances --region=ap-south-1'
                        echo "hello-world-as"
                    }
            }
        }
    }
}
