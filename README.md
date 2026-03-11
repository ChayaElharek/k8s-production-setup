# ☸️ k8s-production-setup

Aplicação Node.js deployada no Kubernetes (k3s) com boas práticas de produção.

## O que foi implementado

- 2 réplicas com load balancing automático
- Health checks (liveness e readiness probes)
- Self-healing — Pod deletado é recriado automaticamente
- Resource limits (CPU e memória)
- Ingress com Traefik

## Evidências

### Pods rodando
<img width="1334" height="220" alt="image" src="https://github.com/user-attachments/assets/7fdcdc30-2e7d-4557-9f4b-35f1b9b01898" />


### Self-healing em ação
<img width="1334" height="220" alt="image" src="https://github.com/user-attachments/assets/553b3cd0-6afe-477a-a830-4099f679eab7" />


## Como rodar
```bash
kubectl apply -f k8s/base/namespace.yaml
kubectl apply -f k8s/base/deployment.yaml
kubectl apply -f k8s/base/service.yaml
kubectl apply -f k8s/base/ingress.yaml
```
