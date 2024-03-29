# Deploy RHODF on RHOCP cluster

## Files

namespace-openshift-storage.yaml - Creates namespace
operatorgroup-openshift-storage-operatorgroup.yaml - Creates the operatorgroup
subscription-odf-operator.yaml - Adds the subscription to the cluster
storagecluster-ocs-storagecluster.yaml - Deploys the storage cluster

*NOTE:
====
A minimum of three nodes must be labeled with `cluster.ocs.openshift.io/openshift-storage: ''`

## Label nodes

`oc label node <NodeName> cluster.ocs.openshift.io/openshift-storage=''`

## Create `openshift-storage` namespace

`oc apply -f namespace-openshift-storage.yaml`

## Create operator group

`oc apply -f operatorgroup-openshift-storage-operatorgroup.yaml`

## Deploy RHODF operator

`oc apply -f subscription-odf-operator.yaml`

## Deploy storage cluster

`oc apply -f storagecluster-ocs-storagecluster.yaml`
