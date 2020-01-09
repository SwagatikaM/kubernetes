# kubernetes

RUNNING PODS -

Commands -
 - kubectl get nodes
 - kubectcl get pods --all-namespaces -o wide
 - kubectl describe pod
 - kubectl get namespaces
 
 cat << EOF | kubectl create -f -
  apiVersion: v1
  kind: Pod
  metadata:
    name: nginx
  spec:
    containers:
    - name: nginx
      image: nginx
  EOF
 
 - kubectl get pod nginx
 
 
 API PRIMITIVES -
 
 Commands -
  - kubectl get componentstatus
  
