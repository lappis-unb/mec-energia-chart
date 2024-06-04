

## Secrets

Substitua "SUBSTITUA_POR_UMA_SECRET_KEY" do Django.

```yaml
kubectl -n mec-energia apply -f - <<EOF
apiVersion: v1
kind: Secret
metadata:
  name: mec-energia-api-secretkey
stringData:
  DJANGO_SECRET_KEY: SUBSTITUA_POR_UMA_SECRET_KEY
EOF
```

Configuração do PostgreSQL. Substitua SUBSTITUA_POR_UM_HOST, SUBSTITUA_POR_UM_PASSWORD, SUBSTITUA_POR_UM_PORT, SUBSTITUA_POR_UM_USER e SUBSTITUA_POR_UMA_VERSAO.

```yaml
kubectl -n mec-energia apply -f - <<EOF
apiVersion: v1
kind: Secret
metadata:
  name: mec-energia-db-connection
stringData:
  POSTGRES_DB: mec_energia
  POSTGRES_HOST: SUBSTITUA_POR_UM_HOST
  POSTGRES_PASSWORD: SUBSTITUA_POR_UM_PASSWORD
  POSTGRES_PORT: SUBSTITUA_POR_UM_PORT
  POSTGRES_USER: SUBSTITUA_POR_UM_USER
  POSTGRES_VERSION: SUBSTITUA_POR_UMA_VERSAO
EOF
```

