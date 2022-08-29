# echo-k8s-app
Kubernetes Argo CD echo application. Select ArgOCD Community Operator for installation from operatorHub


https://operatorhub.io/operator/argocd-operator

On kubernetes, you can install using follwing command:

```
kubectl create namespace argocd

kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

To get the admin password, use the following command:

kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo

```

To get the login password:

$ kubectl get secret argocd-cluster -n argocd -ojsonpath='{.data.admin\.password}' | base64 --decode

Create a new Application from UI:

1. Give a unique Application Name
2. Select project name as  default
3. In the Source section, select this git repo and path as kubernetes
4. Select destination as https://kubernetes.default.svc and namespace as target namesapce where the application can be dpeployed,
5. Once the application is deployed, make some changes by changing the replica to 2 counts and watch the pod scale upto 2 instances.



