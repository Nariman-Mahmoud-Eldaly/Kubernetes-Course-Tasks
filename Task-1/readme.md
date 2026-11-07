## curl -LO https://github.com/kubernetes/minikube/releases/latest/download/minikube-linux-amd64

<img width="1456" height="126" alt="image" src="https://github.com/user-attachments/assets/4e8116e3-1455-4506-8ec2-275d75df098f" />
 minikube start --driver=docker
<img width="1451" height="510" alt="image" src="https://github.com/user-attachments/assets/696e8674-7aa7-4531-a647-f07f3a7df934" />
 minikube start --nodes 3 --cni=calico --cpus 2 --memory 2200
<img width="1452" height="482" alt="image" src="https://github.com/user-attachments/assets/074b0fb2-f24a-44f7-905d-136628a6d527" />
 curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
<img width="1456" height="255" alt="image" src="https://github.com/user-attachments/assets/a5354f21-aeee-490a-aba9-f6f86e65ce8f" />
 kubectl create namespace webapp
 kubectl get namespaces
<img width="885" height="208" alt="image" src="https://github.com/user-attachments/assets/5a7a9ffd-9452-488b-aad5-c772b34c85ae" />
 kubectl apply -f deployment.yaml
 kubectl get pods -n webapp -w
<img width="968" height="436" alt="image" src="https://github.com/user-attachments/assets/0ec34175-b5fe-46bf-9c3c-b5c6eff6cd05" />
 kubectl logs deploy/web-deployment -n webapp -c init-done
<img width="1145" height="60" alt="image" src="https://github.com/user-attachments/assets/fdf715ee-9f78-4816-917a-fb2794f36e5d" />
 kubectl exec deploy/web-deployment -n webapp -c time-updater -- ps


## After Change the init container command so it exits with code 1:
## command: ["sh", "-c", "echo 'init failed'; exit 1"]

<img width="1102" height="580" alt="image" src="https://github.com/user-attachments/assets/b2e29c53-024d-4a91-8ba8-97a9e82dc724" />
  after we fix it 
 <img width="1300" height="271" alt="image" src="https://github.com/user-attachments/assets/4280d165-0ff8-489b-9a5a-5ecc805657b6" />

 <img width="1425" height="696" alt="image" src="https://github.com/user-attachments/assets/cad497a5-d252-4571-a84e-65707bf2eb30" />
