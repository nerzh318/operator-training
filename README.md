# operator-training

## Kubernetes Operators by Jason Dobies and Joshua Wood (O’Reilly). Copyright 2020 Red Hat, Inc., 978-1-492-04805-3

https://www.redhat.com/cms/managed-files/cl-oreilly-kubernetes-operators-ebook-f21452-202001-en_2.pdf

### 1 . Setup Minikube cluster

```
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64   && chmod +x minikube
sudo install minikube /usr/local/bin/

minikube start --vm-driver=virtualbox

curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl

kubectl version 
```

### 2 . Install Operator SDK 

```
RELEASE_VERSION=v0.15.2
curl -LO https://github.com/operator-framework/operator-sdk/releases/download/${RELEASE_VERSION}/operator-sdk-${RELEASE_VERSION}-x86_64-linux-gnu
chmod +x operator-sdk-${RELEASE_VERSION}-x86_64-linux-gnu && sudo mkdir -p /usr/local/bin/ && sudo cp operator-sdk-${RELEASE_VERSION}-x86_64-linux-gnu /usr/local/bin/operator-sdk && rm operator-sdk-${RELEASE_VERSION}-x86_64-linux-gnu
```

### X. Idea for custom Operator : load generation on cluster (poping containers randomly on multiple nodes - those containers shall generate cpu and memory load) - Definition : min containers - max containers - min time container exists
