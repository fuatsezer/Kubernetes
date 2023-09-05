# Minikube
Minikube'ü başlatmak için aşağıdaki komutu çalıştırın.
```console
(base) [train@localhost bin]$ minikube start
```
Minikube docker konteyneri olarak çalıştığını görme komutu
```console
(base) [train@localhost ~]$ docker ps
```
kubectli kurmak için aşağıdaki komutları kullanın
```console
(base) [train@localhost ~]$ curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
(base) [train@localhost ~]$ sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
(base) [train@localhost ~]$ chmod +x kubectl
(base) [train@localhost ~]$ mkdir -p ~/.local/bin
(base) [train@localhost ~]$ mv ./kubectl ~/.local/bin/kubectl
```
cluster hakkında bilgi veren komut
```console
(base) [train@localhost ~]$ kubectl cluster-info
```
nodeları listeleyen komut
```console
(base) [train@localhost ~]$ kubectl get nodes
```
podları listeleyen komut
```console
(base) [train@localhost ~]$ kubectl get pods
```
herşeyi listeleme
```console
(base) [train@localhost ~]$ kubectl get all
```
Bir deployment yaratma
```console
(base) [train@localhost ~]$ kubectl create deployment hello-minikube --image=k8s.gcr.io/echoserver:1.4
```
deploymentı bir ip'ye expose etme
```console
(base) [train@localhost ~]$ kubectl expose deployment hello-minikube --type=NodePort --port=8080
```
deployment'ı silme
```console
(base) [train@localhost ~]$ kubectl delete service/hello-minikube deployment.apps/hello-minikube
```




