








# namespace commands

# kubectl get <kind> -n <namespace name>    
# kind = service, configmap, pod, secret etc
# kubectl get configmap -n my-namespace

output
kube-root-ca.crt    1      8m43s
mongodb-configmap   1      7m21s
nginx-configmap     1      6s

# get the yaml configration of any kind

# kubectl get <kind> -o yaml


# kubens : to change active namespace 

# install kubectx

sudo snap install kubectx --classic


# check the active name-space
kubens

# change the active name-space

kubens my-namespace

# to check the changed active name space again type kubens


