pipeline
{
    agent any
    stages{
        stages ('scm checkout')
    {steps{git 'https://github.com/HarrisKabala/mavenproject.git' }
}
        stages ('code compile')
        {steps {sh 'mvn compile'}}

        stages ('unit test')
        {steps {sh 'mvn test'}}

        stages ('execute test')
        {steps {sh 'mvn verify'}}

        stages ('code build')
        {steps {sh 'mvn package'}}
    }
}
