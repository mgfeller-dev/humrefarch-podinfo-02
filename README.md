# Podinfo - Humrefarch-podinfo-02

The workload is the `podinfo` container image.

[Score](https://score.dev/) is used to deploy the workload locally with `score-compose` in Docker, with `score-k8s` in Kubernetes or with `humctl` in Humanitec. See [Makefile](Makefile) for more details.

## Deploying

Locally:
```bash
make compose-up

make compose-test
```

In Kubernetes (`Kind`):
```bash
make kind-create-cluster

make kind-load-image

make k8s-up

make k8s-test
```

In Humanitec:
```bash
humctl login

humctl config set org FIXME
humctl config set app humrefarch-podinfo-02
humctl config set app development

make htc-up
```
