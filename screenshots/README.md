# Screenshots
To help review your infrastructure, please include the following screenshots in this directory::

## Web Application URL
* http://a75b106ce83824dc3931825df914cd0b-2026840911.us-east-1.elb.amazonaws.com/

## Deployment Pipeline
* DockerHub showing containers that you have pushed
![alt text](./DockerHub.png)
* GitHub repository’s settings showing your Travis webhook (can be found in Settings - Webhook)
![alt text](./Github-Travis.png)
* Travis CI showing a successful build and deploy job
![alt text](./TravisCI-1.png)
![alt text](./TravisCI-2.png)

## Kubernetes
* To verify Kubernetes pods are deployed properly
```bash
kubectl get pods
```
![alt text](./K8s-GetPods.png)

* To verify Kubernetes services are properly set up
```bash
kubectl describe services
```
![alt text](./K8s-DescribeServices.png)

* To verify that you have horizontal scaling set against CPU usage
```bash
kubectl describe hpa
```
![alt text](./K8s-DescribeHPA.png)

HPA responding under Load Generator load
![alt text](./K8s-DescribeHPA-1.png)

* To verify that you have set up logging with a backend application

Feed API Service Logs
```bash
kubectl logs api-feed-597fc75785-4cdjt
```
![alt text](./K8s-Logs-API-Feed.png)

User API Service Logs
```bash
kubectl logs api-user-dfb47fc7c-22rfj
```
![alt text](./K8s-Logs-API-User.png)

Frontend Service Logs
```bash
kubectl logs app-front-844b9c4bff-5x749
```
![alt text](./K8s-Logs-Frontend.png)

Reverse Proxy Logs
```bash
kubectl logs reverse-proxy-7d5576b799-slk2m 
```
![alt text](./K8s-Logs-ReverseProxy.png)