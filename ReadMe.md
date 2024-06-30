
# DataZip Assignment: Superset with Kubernetes Setup

## Installations and Setup
* Install Minikube from thier official website
* Install Docker from their official website

## Execution Process
1. Start Minikube in any terminal
```bash 
minikube start --driver=docker
```
2. Apply Kubernetes Configuration Files Apply all four YAML files using:
```bash
kubectl apply -f <file-name>.yaml
```
3. In my case the commands were:
```bash
kubectl apply -f config-superset.yaml
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl apply -f stateful.yaml
```
4. Check Pod Status Verify all pods are running:
```bash
kubectl get pods
```
5. Check Services List all services:
```bash
kubectl get services
```
6. Obtain the Superset service URL:
```bash
minikube service superset
```
7. Login to Superset Open the URL provided in step 8 in your web browser and log in to Superset.
8. Add ClickHouse Database
* Navigate to Data > Databases > + Database
* Select "ClickHouse" from the database list
9. Configure ClickHouse Connection Fill in the following details:
* Host
* Port
* Database
* Username
10. Establish Connection Click the "Connect" button to establish the connection to ClickHouse.
![alt text](<ClickHouse Connect(Superset).jpg>)