node{

    stage('SCM Checkout')
    {
        git credentialsId: '4cc785e9-441d-4818-a248-2bfb2148004d', url: 'https://github.com/VardhanNS/phpmysql-app.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'dockerHub', variable: 'DHPWD')]) 
        {
            sh "docker login -u nagaraju0669 -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "nagaraju0669" -p "Raju@0669" docker.io'
             //sh 'sudo docker push nagaraju0669/mysql'
             //sh 'sudo docker push nagaraju0669/job1_web1.0'
             sh 'sudo docker push nagaraju0669/job1_web2.0'
            // sh 'docker push nagaraju0669/mysql'
          
    }
}
