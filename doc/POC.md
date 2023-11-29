![2023-11-29 15-46-48](https://github.com/neshchadym/AsciiArtify/assets/70287671/7f5c6604-7db8-4497-b052-3574771631d5)

- k3d cluster create argo
- k cluster-info
- k version
- k get all -A
- k create namespace argocd
- k get ns
- k apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
- k get all -n argocd
- k get po -n argocd -w
- k port-forward svc/argocd-server -n argocd 8080:443&
- k -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
- argo: https://127.0.0.1:8080 u: admin p: above command output
