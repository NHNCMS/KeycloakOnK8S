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

```