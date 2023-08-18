pipeline {

    agent any



       stages {


       stage("Build Modules & Build Docker Images") {

       steps {

       script {

       // def modules = findFiles(glob: '**/pom.xml')

       def modules = ['GymApplicationWithKafka', 'GymReportsApplication','NotificationService','GymAuthenticationService-1','GatewayServer','EurekaServer','GymCommons']

       for (def module in modules) {

       dir("${module}") {

       echo "Building ${module}..."

       bat "mvn clean install"
       }
       }
       }
       }
       }
       }
       }