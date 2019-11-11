# k8sv

1.Add to local machine in /etc/hosts/

172.42.42.101 k8s-node-1
172.42.42.100 k8s-head
172.42.42.102 k8s-node-2



2.Get cluster with two nodes on Flannel network:

vagrant up





From master node:
3.Create namespace

kubectl create namespace monitoring


4.Add Cluster Role for prometheus

kubectl apply -f https://raw.githubusercontent.com/YAD87/k8sv/master/p-clusterrole.yml

5.Add config-map for prometheus

kubectl apply -f https://raw.githubusercontent.com/YAD87/k8sv/master/cm3.yaml

6.Add deployment for prometheus

kubectl apply -f https://raw.githubusercontent.com/YAD87/k8sv/master/p-deployment.yml

7.Add service for prometheus

kubectl apply -f https://raw.githubusercontent.com/YAD87/k8sv/master/p-service.yml

8. Deploy kube-state-metrics
git clone https://github.com/devopscube/kube-state-metrics-configs.git
kubectl apply -f kube-state-metrics-configs/



