# My Helm Charts

### Charts
- nginx-hello
- universal
- pgadmin4

### Add the helm repository
```sh
# add the repository
helm repo add nandras95 https://nandras95.github.io/helm/

# search in the repository
helm search repo nandras95

# search in the repository with all versions
helm search repo nandras95 -l

# update your local repositories
helm repo update

# install from the helm repository
helm install nginx-hello nandras95/nginx-hello --version 0.0.1 -f my-values.yaml
```

### "Check out and use" method
```sh
# clone the repository and go to its folder
helm upgrade --install -f my-values.yaml --set name=nginx-hello nginx-hello ./nginx-hello
```

### Generate index.yaml
This command needs me to update `index.yaml`.
```sh
helm repo index --url https://nandras95.github.io/helm/ .
```
