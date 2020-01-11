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
  - kubectl get pods --show-labels
  - kubectl label pods <podname> env=PROD
  - kubectl get pods -L env
  - kubectl annotate deployment <deployment_name> com.mycompanysomeannotation="Swagatika"
  - kubectl get pods --field-selector status.phase=Running
 
 
 SERVICES -
 Commands -
 - kubectcl get service <service_name>
 - kubectc create -f my-service.yaml
 
  kind: Service
metadata:
  name: my-service
spec:
  selector:
    app: MyApp
  ports:
    - protocol: TCP
      port: 80
      targetPort: 9376
 - curl localhost:30080
  
