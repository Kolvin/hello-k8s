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

# ReplicaSet || Pod/Service Scaling
1. Launch ReplicaSet for multiple webserver pods
   1. kubectl create -f replicaset/replicaset.yml
2. Scale pod count up and down
   1. kubectl replace -f replicaset/replicaset.yml || kubectl edit replicaset