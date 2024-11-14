# pods creation
we can create one ec2 instace
![Screenshot 2024-11-14 235950](https://github.com/user-attachments/assets/13d7f942-0348-4f16-9fff-d6a34c4be1f1)

sudo su -

apt update -y

# install docker

sudo curl -fsSL https://get.docker.com -o get-docker.sh 

![Screenshot 2024-11-14 234116](https://github.com/user-attachments/assets/da2813c0-7b56-4580-9e73-e08e0ca3a0ce)

# we need permison aslo
chmod 700 get-docker.sh

/.get docker.sh
# docker version

systemctl status docker
![Screenshot 2024-11-14 234315](https://github.com/user-attachments/assets/bf7807c0-b94f-4e11-83b7-a1e3610aa50e)

https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 

ll
sudo mv minikube-linux-amd64 /usr/local/bin/minikube

sudo chmod +x /usr/local/bin/minik be

sudo minikube version

sudo apt install curl wget apt-transport-https -y

sudo curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

sudo kubectl version --client

sudo curl -LO "https://dl.k8s.io/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"
sudo echo "$(cat kubectl.sha256) kubectl" | sha256sum --check
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

sudo kubectl version --client

sudo kubectl version --client --output=yaml

sudo minikube start --driver=docker --force

creation of pod

kubectl run pod1 --image=nginx

kubectl get pods

vi srinu.yml

apiVersion: v1

kind: Pod

metadata:

  name: nginx
  
spec:

containers:

  - name: nginx

    image: nginx:1.14.2
    
    ports:
    
    - containerPort: 80
      
kubectl create -f srinu.yml

kubectl get pods

![Screenshot 2024-11-14 235751](https://github.com/user-attachments/assets/b59aa89c-1a1e-42d5-a0c9-36f699fa2780)
![Screenshot 2024-11-14 235545](https://github.com/user-attachments/assets/839c4a35-3f19-4692-9c43-15841d57f8d5)




