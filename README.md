## CREATE 

kubectl port-forward \
$(kubectl get pods -l app=frontend -o jsonpath='{.items[0].metadata.name}') \
8080:8080
frontend-deployment-685f4f6778-25hvp

kubectl create deployment hello-minikube --image=k8s.gcr.io/echoserver:1.10

kubectl expose deployment hello-minikube --type=NodePort --port=8080

minikube service hello-minikube --url

## DELETE 

kubectl delete services hello-minikube
kubectl delete deployment hello-minikube

Proactive monitoring
Cluster visibility and capacity planning
Trigger alerts and notification
Metrics dashboards

---- Nginx Example ----
The ServiceMonitor will select the NGINX pod, using the matchLabels selector