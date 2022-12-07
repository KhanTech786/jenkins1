pipeline{
    agent any
    environment{
        myvar='myvalue'
    }
    parameters{
        string(name:'name',defaultValue:'aiyman',description:'')
        choice(name:'work',choices:['developer','admins'], description:'')
        booleanParam(name:'applied', defaultValue:false, description:'')
    }
    stages{
        stage("build"){
            agent {
                label 'win'
            }
            steps{
                echo "this is the build stage ${myvar}"
            }
        }
        stage("test"){
            steps{
                echo "this is the test stage ${params.name}"
            }
        }
    }
    post{
        always{
            echo "this will always work"
        }
    }
}
