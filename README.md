# echo-k8s-app
Kubernetes Argo CD echo application. Select ArgOCD Community Operator for installation from operatorHub


https://operatorhub.io/operator/argocd-operator

To get the login password:

$ kubectl get secret argocd-cluster -n argocd -ojsonpath='{.data.admin\.password}' | base64 --decode

Create a new Application from UI:

1. Give a unique Application Name
2. Select project name as  default
3. In the Source section, select this git repo and path as kubernetes
4. Select destination as https://kubernetes.default.svc and namespace as target namesapce where the application can be dpeployed,
5. Once the application is deployed, make some changes by changing the replica to 2 counts and watch the pod scale upto 2 instances.
6. 


