# ☸️ k8s-production-setup

Aplicação Node.js deployada no Kubernetes (k3s) com boas práticas de produção.

## O que foi implementado

- 2 réplicas com load balancing automático
- Health checks (liveness e readiness probes)
- Self-healing — Pod deletado é recriado automaticamente
- Resource limits (CPU e memória)
- Ingress com Traefik

## Evidências

## Cluster Status

Pods running in the cluster:

![Pods Running](images/pods-running.png)

## Self Healing Demonstration

Kubernetes automatically recreating failed pods:

![Self Healing](images/self-healing.png)


## Como rodar
```bash
kubectl apply -f k8s/base/namespace.yaml
kubectl apply -f k8s/base/deployment.yaml
kubectl apply -f k8s/base/service.yaml
kubectl apply -f k8s/base/ingress.yaml
```
