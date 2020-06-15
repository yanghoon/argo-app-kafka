## Test
```bash
helm template . -n api
helm template . -n api-aks
```

## Test
```bash
argocd app delete api
helm template . -n api | argocd app create api -f -
# argocd app create api \
#   --repo https://yanghoon.github.io/charts --helm-chart argo-app --revision 0.3.1 --values "$(cat values.yaml)" \
#   --dest-namespace default --dest-server https://kubernetes.default.svc
```# argo-app-kafka
