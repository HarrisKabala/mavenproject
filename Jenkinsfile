pipeline
{
    agent any
    stages{
        stage ('scm checkout')
    {steps {git 'https://github.com/HarrisKabala/mavenproject.git' }
}
        stage ('code compile')
        {steps {sh 'mvn compile'}}

        stage ('unit test')
        {steps {sh 'mvn test'}}

        stage ('execute test')
        {steps {sh 'mvn verify'}}

        stage ('code build')
        {steps {sh 'mvn package'}}

        post {
    success {
        echo 'Build succeeded!'
    }
    failure {
        echo 'Build failed!'
    }
}


    }
}
