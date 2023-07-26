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

Télécharger et installer [Docker Desktop for Windows](https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe).

### Installation de Minikube

:notebook: Référence : <https://minikube.sigs.k8s.io/docs/start/>

```python
# Download
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

# Install
sudo install minikube-linux-amd64 /usr/local/bin/minikube

# Start
minikube start
```
