# Public_Challenge_Kubernetes


  
Step 1: Install and Setup Kubectl
  Follow the instructions in https://kubernetes.io/docs/tasks/tools/install-kubectl

Step 2: Install a HyperVisor.
  Follow the installation instructions in https://www.virtualbox.org/manual/ch02.html
  
Step 3: Setup Minikube in desktop.
  Follow the below instructions to install minikube on respective platforms.
  https://kubernetes.io/docs/tasks/tools/install-minikube/
  
Step 4: After successful installation and minicube started.
  Run following commands to check cluster status.
  # kubectl get all
  # kubectl get nodes
  # kubectl cluster-info
  
Step 5: Copy the deployment.yaml file to a path and apply.
  # kubectl apply -f .\nginx-hello-world-deployment.yaml
  
Step 6: Check deployment is successful and both pods are rolled out.
  # kubectl get pods
  
Step 7: Expose the service to external access.
  # kubectl expose deployment nginx-hello-world1 --type=NodePort --port=80
  
Step 8: Verify Service and get service url using minikube.
  # kubectl get service
  # minikube service nginx-hello-world1 --url
    http://192.168.99.100:31563
    
Step 9: Verify the URL hits the service from desktop browser.  
  
  
