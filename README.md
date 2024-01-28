# RESOURCE MONITOR App Using Python Run on Cloud Native!
This project aim is to learn:
- create an functional app using pyhon language with flask and psutil
- how to containerize python application
- creating dockerfile
- build a docker image
- running docker container
- create ECR (Elastic Container Registry) repository and push docker image into ECR from terminal using Boto3
- create EKS (Elastic Kubernetes Service) cluster and nodegroup.
- create kubernetes deployment and service using python!

## Project Requirements
- Python Installed.
- AWS Account.
- Programmatic access and AWS configured with CLI.
- Docker desktop.
- Kubectl installed.
- Code Editor.

### **Step 1: Clone the code**

Clone the code from the repository:

```
git clone <repository_url>
```

### **Step 2: Install dependencies**

This application uses **`psutil`**, **`Flask`, **`Plotly`**, `boto3`** libraries. Install them using pip:

```
pip3 install -r requirements.txt
```

### **Step 3: Run the application**

To run the application, navigate to the root directory of the project and execute the following command:

```
python3 app.py
```

This will start the Flask server on **`localhost:5000`**.

### **Step 4: Build the Docker image**

To build the Docker image, execute the following command:

```
docker build -t <image_name> .
```

### **Step 5: Run the Docker container**

To run the Docker container, execute the following command:

```
docker run -p 5000:5000 <image_name>
```

This will start the Flask server in a Docker container on **`localhost:5000`**. 

### **Step 6: Push the Docker image to ECR**

Push the Docker image to ECR using the push commands on the console:

```
docker push <ecr_repo_uri>:<tag>
```

### **Step 7: Create an EKS cluster**

Create an EKS cluster and add node group

### **Step 8: Create a node group**

Create a node group in the EKS cluster.

### **Step 9: Create deployment and service**

- Once you run this file by running “python3 eks.py” deployment and service will be created.
- Check by running following commands:

```jsx
kubectl get deployment -n default (check deployments)
kubectl get service -n default (check service)
kubectl get pods -n default (to check the pods)
```

Once your pod is up and running, run the port-forward to expose the service

```bash
kubectl port-forward service/<service_name> 5000:5000
```
