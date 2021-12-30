# hello-k8s
Hello world project where im learning kubernetes using [KodeKloud](https://kodekloud.com/)
___

Running a cluster locally using the following tools
1. [minikube](https://minikube.sigs.k8s.io/docs/start/)
2. [OhMyZSH](https://github.com/ohmyzsh/ohmyzsh) with the following plugins, provides useful kubectl [shortcuts](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/kubectl)
```shell
plugins=(
    git
    docker
    docker-compose
    zsh-autosuggestions
    zsh-completions
    kubectl
)
```
___

# [ReplicaSet](https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/) || Pod/Service Scaling
1. Launch ReplicaSet for multiple webserver pods
   1. kubectl create -f replicaset/replicaset.yml
2. Scale pod count up and down
   1. kubectl replace -f replicaset/replicaset.yml || kubectl edit replicaset

# [Deployments](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/) || Managed Services
1. Launch Deployment for multiple api service
   1. kubectl create -f deployments/api.yml
2. Update deployment (replicas and images)
   1. kubectl edit deployment api-deployment
   2. kubectl apply -f deployments/api.yml
3. Deployment Info and Debugging 
   1. kubectl rollout status deployment
   2. kubectl describe deployment api-deployment

# [Services](https://kubernetes.io/docs/concepts/services-networking/service/) 
1. Create NodePort & ClusterIP for webserver
   1. kubectl create -f services/webserver-service.yml
   1. kubectl create -f services/webserver-clusterip.yml