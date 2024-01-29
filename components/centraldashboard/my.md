##

node 14.21.3



sudo yum install -y epel-release
sudo curl -sL https://rpm.nodesource.com/setup_14.x | sudo bash -
sudo yum install -y nodejs



[root@master1 centraldashboard]# node -v
v14.21.3
[root@master1 centraldashboard]# npm -v
6.14.18
[root@master1 centraldashboard]#


## image build & push
cd kubeflow/components/centraldashboard
make docker-build docker-push IMG=sjw451/centraldashboard TAG=v1.8.0-rc.0


## deploy to the  cluster




kubectl port-forward --address 0.0.0.0 svc/istio-ingressgateway -n istio-system 
user@example.com
12341234
