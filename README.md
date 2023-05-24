**Kubernetes demo environment**
This repository contains a simple kubernetes configuration with one node js app.
The web app is related to a mongo image when user data is persisted through a web form.
In order to run this you shoould already have installes Minikube from https://minikube.sigs.k8s.io/docs/start/.

Once installed minikube go to the root directory and run the following commands:
- kubectl apply -f mongo-config.yaml
- kubectl apply -f mongo-secret.yaml
- kubectl apply -f mongo.yaml
- kubectl apply -f webapp.yaml

To be sure that all is correctly set, run the command:
- kubectl get svc
You should see the details about the services running, then run the command
To retrieve the IP to be used in the browser and access the webapp landing page,
run the command 
- kubectl get node -o wide 
copy and paste the IP:30300 into the browser.
