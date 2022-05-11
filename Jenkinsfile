pipeline {

    agent any

    stages{

        stage("Build Vote,Worker,Result Apps"){
          steps {
              script {
                  echo "Building Images"
                //   sh "docker build -t raju/voting-app -f vote/Dockerfile"
                //   sh "docker build -t raju/worker-app -f worker/Dockerfile"
                //   sh "docker build -t raju/result-app -f result/Dockerfile"
              }
          }

        }
        stage("Run CodeAnalysis"){
          steps {
              script {
                  dir ('vote'){
                       echo "Running CodeAnalysis"
                       //sh "./sonar-scanner"
                  }
                  dir ('wroker'){
                       echo "Running CodeAnalysis"
                       //sh "./sonar-scanner "
                  }
                dir ('result'){
                       echo "Running CodeAnalysis"
                       //sh "./sonar-scanner"
                  }
              }
          }

        }
        stage("Push Vote,Worker,Result Images to registry"){
          steps {
              script {
                  echo "Building Images"
                //   sh "docker push raju/voting-app"
                //   sh "docker push raju/worker-app"
                //   sh "docker push raju/result-app"
              }
          }

        }

        stage("Deploy the Application on k8s"){
          steps {
              dir ('k8s'){
                  echo "Deploy Apps innto k8s"
                //   sh """
                //      export KUBECONFIG=./config
                //      kubeclt apply -f voting-app.yaml
                //      kubectl apply -f voting-svc.yaml
                //      kubeckt apply -f redis-app.yaml
                //      kubectl apply -f redis-svc.yaml
                //      kubectl apply -f worker-app.yaml
                //      kubectl apply -f postegres-db.yaml
                //      kubectl apply -f db-svc.yaml
                //      kubectl apply -f result-app.yaml
                //      kubectl apply -f result-svc.yaml
                //   """

              }
             
          }

        }

    }

}