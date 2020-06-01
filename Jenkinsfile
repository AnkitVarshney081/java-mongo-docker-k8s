node{
   stage("Git Clone"){
       git credentialsId: '3c57c31d-7e69-4389-828b-f27eab7cb945', url: 'https://github.com/AnkitVarshney081/java-mongo-docker-k8s.git'
   }
   stage("Maven Clean Build"){
       def mavenHOME = tool name: "maven3", type: "maven"
       def mavenCMD = "${mavenHOME}/bin/mvn "
       sh "${mavenCMD} clean package"
   }
   stage("Build Docker Image"){
       sh "docker build -t dockerhandson/spring-boot-mongo ."
   }
}
