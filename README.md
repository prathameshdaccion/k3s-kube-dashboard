# k3s-kube-dashboard

#### Steps

1. Clone repository using below command

###### Command

$ git clone https://github.com/prathameshdaccion/k3s-kube-dashboard.git

$ cd k3s-kube-dashboard/

2. Apply config file

###### Command

$ kubectl create -f kube-dashboard.yaml

3. Validate Deployment

###### Command

$ kubectl -n kubernetes-dashboard get all

4. Access Kube-Dashboard using External-IP of kubernetes-dashboard service and 8081 port

URL: https://External-IP:8081

5: Extract token for dashboard login

###### Command

$ kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin-user | awk '{print $1}')

6. Validate your K3S cluster on Dashboard.

