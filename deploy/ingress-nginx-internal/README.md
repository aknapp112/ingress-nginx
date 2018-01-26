# ingress-nginx-internal
Kubernetes configuration to run a _second_ nginx ingres controller using a seperate namespace and controller class.

## Overview
The configuration files contained here create a new namespace of _ingress-nginx-internal_ as well as a new ingress class called _nginx-internal_ that you can use with an Ingress to bind the service to a seperate ingress controller that you can use for private ingress.


## Deployment

```console 
kubectl create -f namespace.yaml

kubectl	create -f default-backend.yaml

kubectl create -f configmap.yaml

kubectl create -f tcp-services-configmap.yaml

kubectl create -f udp-services-configmap.yaml

kubectl create -f rbac.yaml

kubectl create -f with-rbac.yaml

```


