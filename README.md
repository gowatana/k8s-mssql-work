# MS SQL Server on k8s 

# 0. Create Secrets

create sa password.

```
$ echo -n VMware1! | base64
Vk13YXJlMSE=
$ vi 00_secrets.yml
$ kubectl apply -f 00_secrets.yml
```
# 1. create PVC.

```
$ kubectl apply -f 01_mssql_pvc.yml
```

# 2. create Deployments.

```
$ kubectl apply -f 02_mssql_deploy.yml
```

