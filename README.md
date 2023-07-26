# DEVOPS

Guides sur la thématique DEVOPS (Linux, Docker, K8S, Minikube, Helm, Anthos...)

## Guides

### Installation Linux Ubuntu sur Windows 10

`TODO`

### Configuration Linux Ubuntu

`TODO`

### Installation de Docker

> :bulb: L'idée : installer Docker Desktop sur l'hôte Windows 10 et exploiter le WSL 2 pour l'intégration avec Linux Ubuntu

:notebook: Référence : <https://docs.docker.com/desktop/wsl/>

Depuis **Windows**, télécharger, installer [Docker Desktop for Windows](https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe) et cocher la case WSL (2).

Depuis **Ubuntu** et **Windows**, tester l'installation avec la même commande :

```python
# Télécharger et exécuter une image Docker
docker run hello-world
```

### Installation de Minikube

> Références :
>
> - :notebook: <https://minikube.sigs.k8s.io/docs/start/>
> - :notebook: <https://minikube.sigs.k8s.io/docs/handbook/controls/>

```python
# Télécharger
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

# Installer
sudo install minikube-linux-amd64 /usr/local/bin/minikube

# Démarrer
minikube start

# Vérifier
kubectl get po -A

# Forcer minikube à télécharger la version adéquate de kubectl
minikube kubectl -- get po -A

# Lancer le dashboard
minikube addons enable metrics-server
minikube dashboard

# Déployer un serveur avec kubectl
kubectl create deployment hello-minikube --image=kicbase/echo-server:1.0

# Exposer le serveur
kubectl expose deployment hello-minikube --type=NodePort --port=8080

# Ouvrir le serveur dans le navigateur
minikube service hello-minikube

# Démarrer un second cluster
minikube start -p cluster2

# Arrêter un cluster
minikube stop

# Supprimer un cluster
minikube delete

# Arrêter un cluster spécifique
minikube stop -p cluster2

# Supprimer tous les clusters
minikube delete --all
```
