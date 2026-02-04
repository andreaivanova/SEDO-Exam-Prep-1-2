pipeline {
    agent any
    
    stages{
        stage("restore dependendies"){
          when { branch pattern: "(main|develop|feature).*", comparator: "REGEXP" }
           steps{
            bat 'dotnet restore'
           } 
        }

        stage("build the project"){
          when { branch pattern: "(main|develop|feature).*", comparator: "REGEXP" }
           steps{
            bat 'dotnet build'
           } 
        }

         stage("run the tests - test 1"){
           when { branch pattern: "(main|develop|feature).*", comparator: "REGEXP" }
           steps{
            bat 'dotnet test TestProject1 --no-build --verbosity normal'
           } 
        }

          stage("run the tests - test 2"){
          when { branch pattern: "(main|develop|feature).*", comparator: "REGEXP" }
           steps{
            bat 'dotnet test TestProject2 --no-build --verbosity normal'
           } 
        }

            stage("run the tests - test 3"){
            when { branch pattern: "(main|develop|feature).*", comparator: "REGEXP" }
           steps{
            bat 'dotnet test TestProject3 --no-build --verbosity normal'
           } 
        }
        }
}
