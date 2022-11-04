# KeycloakOnK8S

First off, install psql with the following command:

```bash
helm install postgresql bitnami/postgresql \
--set auth.username=admin \
--set auth.password=admin \
--set auth.database=keycloak \
--set primary.persistence.storageClass=scw-bssd-retain \
--namespace keycloak \
--create-namespace
```

One-liner:

```bash
helm install postgresql bitnami/postgresql --set auth.username=admin --set auth.password=admin --set auth.database=keycloak --set primary.persistence.storageClass=scw-bssd-retain --namespace keycloak --create-namespace
```


Cert_manager
```bash
helm repo add jetstack https://charts.jetstack.io

kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.10.0/cert-manager.crds.yaml
```

Keycloak url: https://nhn-keycloak.seproprio.dev/