# Kubers Custom Resource Definition

## Execute the Program

```shell
cargo run
```

## Validate CRD Creation

```shell
kubectl get crd
NAME                     CREATED AT
kcdtrack2s.example.com   2024-09-07T16:25:45Z
```

## Apply the CRD Yaml Definition

```shell
kubectl apply -f kube-manifests/kcdhyd.yaml
kcdtrack2.example.com/integrating-rust created
```

## Print a Specific jsonpath of CRD

```shell
kubectl get kcdtrack2 integrating-rust -o jsonpath='{.spec.speaker}'
Sangam Biradar, CloudNativeFolks
```