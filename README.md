# echo-k8s-app
Kubernetes Argo CD echo application. Select ArgOCD Community Operator for installation from operatorHub


https://operatorhub.io/operator/argocd-operator

$ kubectl get secret argocd-cluster -n argocd -ojsonpath='{.data.admin\.password}' | base64 --decode
