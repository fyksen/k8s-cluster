# Notes about how I installed Flux

* Based on [this](https://fluxcd.io/flux/installation/bootstrap/github/) guide
* Get Github PAT token from [here](https://github.com/settings/tokens?type=beta)

## Bootstrap

* In this example, the github repo is  already created before bootstrapping flux.

```
flux bootstrap github \
  --token-auth \
  --owner=fyksen \
  --repository=k8s-cluster \
  --branch=main \
  --path=k8s
```

