### install helm


```bash
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
chmod 700 get_helm.sh
./get_helm.sh
```
Link 
* [install helm](https://helm.sh/docs/intro/install/)
### enable helm in microk8s

```bash
microk8s enable helm3
```
### add bitnami repo

```bash
helm repo add bitnami https://charts.bitnami.com/bitnami
```

create pg-user secret

```bash
kubectl create secret generic pg-user \
--from-literal=postgres-password='<PGPASSWORD>'
```

install helm chart
```bash
helm install postgres -f k8s/db/values.yaml bitnami/postgresql
```

Link
* [bitnami postgres helm chart](https://bitnami.com/stack/postgresql/helm)