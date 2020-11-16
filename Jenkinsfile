node{

    stage('SCM Checkout')
    {
        git credentialsId: 'git', url: 'https://github.com/Nagaraju0669/e-commerce.git'
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
            sh "docker login -u nagaraju0669 -p ${Raju@8196}"
        }
        sh 'docker push nagaraju0669/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "nagaraju0669" -p "Raju@0669" docker.io'
             //sh 'sudo docker push nagaraju0669/mysql'
             //sh 'sudo docker push nagaraju0669/job1_web1.0'
             sh 'sudo docker push nagaraju0669/job1_web2.0'
            // sh 'docker push nagaraju0669/mysql'
          
    }
}
