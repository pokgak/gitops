# gitops

Repo to store all manifests for homelab cluster and used as the source of truth for flux gitops.

## Token Expiry

Flux controller github token is valid until 31/12/2023. If error then please generate a new token and update the secret in the cluster.

## Bootstrap

https://fluxcd.io/flux/installation/bootstrap/github/#github-personal-account

```
flux bootstrap github \
                        --owner=$GITHUB_USER \
                        --repository=gitops \
                        --branch=main \
                        --path=./clusters/labsV2 \
                        --personal \
                        --token-auth
```
