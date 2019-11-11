# k8sv

Add to local machine in /etc/hosts/

172.42.42.101 k8s-node-1
172.42.42.100 k8s-head
172.42.42.102 k8s-node-2



Get cluster with two nodes on Flannel network:

vagrant up






Create namespace

kubectl create namespace monitoring


Add Cluster Role for prometheus

kubectl apply -f https://raw.githubusercontent.com/YAD87/k8sv/master/p-clusterrole.yml

Add config-map for prometheus

kubectl apply -f https://raw.githubusercontent.com/YAD87/k8sv/master/cm3.yaml

Add deployment for prometheus

kubectl apply -f 

https://raw.githubusercontent.com/YAD87/k8sv/master/p-deployment.yml

Add service for prometheus

https://raw.githubusercontent.com/YAD87/k8sv/master/p-service.yml
