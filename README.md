# Description 

These manifest will setup a nfs dynamic provisioning on k8s cluster. 

# HOWTO

Fist of all apply serviceAccount rbacAuthentication :

kubectl apply -f rbac.yamlserver

For the  storageclass apply provisioner.yaml

kubectl apply -f provisioner.yaml

NOTE: Edit PROVISIONER_NAME & NFS_SERVER ENV in container section , server & path in volumes section and specify your NFS Server Information.

and for the last one apply storage class : 
kubectl apply -f storageclass.yaml.

for the test you can run 4-pvc-nfs.yaml and 4-busybox-pv-nfs.yaml to test your NFS Provisioner.
