# Persistent-Volumes
```
apiVersion: v1
kind: PersistentVolume
metadata:
  name: <Name>
spec:
  capacity:
    storage: 5Gi
  accessModes:
    - ReadWriteOnce
  persistentVolumeReclaimPolicy: Retain
  storageClassName: managed-nfs-storage
  volumeMode: Filesystem
  claimRef: 
    name: postgres-data
    namespace: che
  nfs:
    path: /var/nfsshare/che
    server: <server ip> <192.166.39.14>
 ```
