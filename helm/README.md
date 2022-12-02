# Introduction
This chart is used to deploy AuthAPI in K8S environment. Helm 3.0+ is needed to deploy this chart.

# How to deploy AuthAPI
## Example: Use default values to deploy one AuthAPI.
```
helm install authapi ./authapi
```

## Example: Deploy 2 AuthAPI single pods.
```
helm install authapi ./authapi --set app.replicas=1
```

## Example: Deploy AuthAPI pods in a specific environment value yaml file.
```
helm install authapi ./authapi -f values-uat.yaml
```

# How to remove AuthAPI
```
helm uninstall authapi
```

# How to update AuthAPI
For example, assuming you have already deployed a 3 AuthAPI PODs cluster, and you want to create one more TDV POD, then execute the command below,
```
helm upgrade authapi ./authapi --set app.replicas=4
```