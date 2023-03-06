pipeline 
{
    agent any

    stages 
    {
        stage('Build') 
        {
            steps 
            {
                sh 'mvn clean package'
            }
        }

        stage('Test') 
        {
            steps 
            {
               sh 'mvn test'
            }
        }

        stage('Deploy') 
        {
            steps 
            {
                sh 'mvn deploy'
            }
        }
    }

    post
    {

    	always
    	{
    		emailext body: 'Summary', subject: 'Jenkins Pipeline', to: '2000087361@hexaware.com'
    	}

    }
}
