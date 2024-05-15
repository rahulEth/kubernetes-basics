### install minikube

`curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64`
`sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64`

### kubectl 

`curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl`
   
`sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl`

### starts minikube

`minikube start --vm-driver=docker`
`minikube status`

### kubernetes common commands

`kubectl version`
`kubectl get pod -o wide`
`kubectl get services`
`kubectl get replicaset`
`kubectl describe pod <pod_name>`

### get deployment status

`kubectl get deployment <deployment name> -o yaml`

### access the terminal of the pod

`kubectl exec -it <pod_name> -- bin/bash`

`kubectl logs <pod_name>`

### delete deployment

`kubectl delete deployment <deployment name>`

### edit deployment 

`kubectl edit deployment <deployment name>`

### create deployment 

`kubectl create deployment <dep_name>  --image=<imagenme>`

### get deployment 

`kubectl get deployment`

### config file

`kubectl apply -f config-file.yaml`

### et deployment result

`kubectl get deployment nginx-deployment -o yaml > deployment-result.yaml`

### check pod logs

`kubectl logs mongodb-deployment-6597c98d7-759wv  -c mongodb`

### check all pod status

`kubectl get pod --watch`

`kubectl get all | grep MongoDB`

### below commnad assign external IP to service

`minikube service <service name >`

### namespace commands

`kubectl get <kind> -n <namespace name>`   
`kind = service, configmap, pod, secret etc`

`kubectl get configmap -n my-namespace`

output
kube-root-ca.crt    1      8m43s
mongodb-configmap   1      7m21s
nginx-configmap     1      6s

### get the yaml configration of any kind

`kubectl get <kind> -o yaml`


### kubens : to change active namespace 

### install kubectx

`sudo snap install kubectx --classic`


### check the active name-space

`kubens`

### change the active name-space

`kubens my-namespace`

### to check the changed active name space again 

`kubens`

### install minikube controller in minikube 

`minikube addons enable ingress`

### get name space

`kubectl get ns`

### helm commands

`helm install <chartname>`

### values injection into tehmplate file

`helm install --values=my-values.yaml <chartname>`

`helm upgrate <chartname>`

`helm rollback <chartname>`

### services commands

`kubectl get svc`

### get endpoints

`kubectl get endpoints`






