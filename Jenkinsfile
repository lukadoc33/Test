pipeline {
  agent any
  
 // enviroment{
 //   BUILD_VERSION ='1.0.3'
 // }
  parameters {
    choice(name: 'VERSION', choices:['1.0.1', '1.0.2', '1.0.3'], description:'')
    booleanParam(name: 'ExecuteTests', defaultValue: true, description:'')
  }  
  stages {
    
    stage("build") {
      
          steps {
            echo 'building the application...'
           // echo "Building version ${BUILD_VERSION}"
          }
    }
    stage("test") {
      when {
        expression {
          params.ExecuteTest
        }
      }
           steps {
             echo 'testing the application...'
           }
    }
    stage ("deploy") {
      
          steps{
            echo 'deploy the application...'
            echo "deploying version ${params.VESRION}"
          }
    }
  
 }
}
