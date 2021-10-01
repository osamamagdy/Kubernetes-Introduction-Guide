# MongoDB-kubernetes

# For mongo-deployment
## Secret creation notes

--> to create your secret credentials encoded you can run `echo -n 'my_credential' | base64`
--> then go to terminal and type 
`kubectl apply -f secret.yaml`


## Creating deployment
--> run `kubectl apply -f mongo-deployment.yaml`

# For mongo-express-deployment
##  Configmap creation
--> `database_url` is the name of the service in the mongo-deployment ( as it is what routes traffice and requests)
--> run the command 
    `kubectl apply -f configmap.yaml`

##  Creating deployment
--> run `kubectl apply -f mongo-express-deployment.yaml`

--> you can check logs of connection by `kubectl logs "mongo-express-pod-name"`

# External IP with minikube
--> run `minikube service "mongo-express-service-name"`