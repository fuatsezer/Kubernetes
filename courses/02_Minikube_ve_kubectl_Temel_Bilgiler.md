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
