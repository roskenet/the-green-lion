# The Green Lion

## Minikube Cluster

Um das "richtige" Cloud-Feeling zu simulieren, laufen alle Services in einem Kubernetes-Cluster den ich lokal mit Minikube aufsetze.

Starte einen lokalen Cluster mit 

```sh
mkdir -p $HOME/minikube
minikube start --driver=docker --memory=8192 --cpus=2 --mount --mount-string="$HOME/minikube:/mnt/minikube"
```

Nun koennen wir mit `kubectl get pods` nachsehen, ob der cluster antwortet. Dieser Befehl sollte keine resourcen in unserm neuen Cluster anzeigen.

Nun installieren wir noch das ingress addon:
```sh
minikube addons enable ingress
```

