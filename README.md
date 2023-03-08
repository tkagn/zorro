# zorro


Random Zorro RHOCP Cluster with Kustomize manifests:

 - Red Hat OpenShift Data Foundation (RHODF)
 - Red Hat OpenShift APIs for Data Protection (RHOADP)
 - Red Hat Advanced Cluster Management (RHACM) 
 - Red Hat Advanced Cluster Security (RHACS)
 - Red Hat Quay Container Security Operator (RHQCSO)
 - Red Hat Local Storage Operator (RHLSO)

Set namespace to be managed by ArgoCD:

```bash
oc label namespace <namespace> argocd.argoproj.io/managed-by=openshift-gitops
```
