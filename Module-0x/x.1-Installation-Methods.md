# Setting Up Argo CD - Rollout

```bash
kubectl create namespace argo-rollouts
kubectl apply -n argo-rollouts -f https://github.com/argoproj/argo-rollouts/releases/latest/download/install.yaml
```

- Documentation: https://github.com/argoproj/argo-rollouts/blob/master/docs/installation.md

## For UI Dashboard

### Kubectl Plugin Installation

```bash
curl -LO https://github.com/argoproj/argo-rollouts/releases/latest/download/kubectl-argo-rollouts-linux-amd64
chmod +x ./kubectl-argo-rollouts-linux-amd64
sudo mkdir -p /usr/local/bin/kubectl-argo-rollouts
sudo mv ./kubectl-argo-rollouts-linux-amd64 /usr/local/bin/kubectl-argo-rollouts
kubectl argo rollouts version
```

### Run the Dashboard

- Expose this Port: `sudo ufw allow 3100`

```bash
kubectl argo rollouts dashboard
```

- Access the Dashboard on : `http://<IP>:3100/rollouts`
