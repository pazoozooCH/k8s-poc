# Kubernetes POC

See <https://docs.inftec.ch/display/TEC/Kubernetes> for additional documentation.

## Ingress

### Set up Minikube

```
minikube addons enable ingress
```

### Set up resources

```
kubectl apply -f .\demo-web-ingress.deployment.yaml
kubectl apply -f .\demo-web-ingress.service.yaml
```

Get IP and Port from Minikube: `minikube service demo-web-ingress-service --url`

### Adopt hosts file

Add an entry for *demo-web-ingress.info* to the systems
host file with the IP of minikube (`minikube ip`).

### Access

Access the application at <http://demo-web-ingress.info>
and <http://demo-web-ingress.info/v2>