
node('docker_mvn') {

    stage ('Clone') {
        git url: 'https://github.com/ayanendude/first_spring.git'
    }

    stage ('Build'){
        sh "sleep 1"
        sh "echo 1"
        //mvn
        sh "mvn -DskipTests=true clean install"
    }

    stage ('test'){
        parallel 2:{
        sh "sleep 2"
        sh "echo 2"
        sh "mvn test"
        }, 3:{
        sh "sleep 3"
        sh "echo 3"
        }
    }
}
