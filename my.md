## go

sudo curl -O https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.21.6.linux-amd64.tar.gz


vi ~/.bash_profile
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
export PATH=$PATH:/usr/local/go/bin


## kind or kubernetes

## docker
sudo yum install docker-ce docker-ce-cli  docker-buildx-plugin docker-compose-plugin

containerd.io제외


## kubebuilder
curl -L -o kubebuilder "https://go.kubebuilder.io/dl/latest/$(go env GOOS)/$(go env GOARCH)"
chmod +x kubebuilder && mv kubebuilder /usr/local/bin/

# notebook-controller

## image build & push
cd kubeflow/components/notebook-controller
make docker-build docker-push IMG=sjw451/notebook-controller TAG=v1.8.0-rc.0

** docker.io/kubeflownotebookswg/notebook-controller

:tagname
## deploy to the  cluster

kubectl port-forward --address 0.0.0.0 svc/istio-ingressgateway -n istio-system 
user@example.com
12341234


## image build & push
cd kubeflow/components/notebook-controller
make docker-build docker-push IMG=sjw451/notebook-controller TAG=v1.8.0-rc.0


## deploy to the  cluster

kubectl port-forward --address 0.0.0.0 svc/istio-ingressgateway -n istio-system 
user@example.com
12341234
