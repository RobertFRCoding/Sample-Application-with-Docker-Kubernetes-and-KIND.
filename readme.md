README
This README file provides instructions for launching and using the application using Docker, Kubernetes, and KIND (Kubernetes IN Docker).

Prerequisites
Make sure you have the following components installed on your system:

Docker: https://docs.docker.com/get-docker/
KIND: https://kind.sigs.k8s.io/
Kubernetes: https://kubernetes.io/docs/tasks/tools/
Steps to Launch the Application
Follow the steps below to launch the application using Docker, Kubernetes, and KIND.

Clone the application repository:

> git clone https://github.com/your-user/your-repository.git
> cd your-repository

Build a Docker image:

> docker build -t curso-kind-nodejs:0.0.1 .

This command will create a Docker image tagged as curso-kind-nodejs:0.0.1 using the provided Dockerfile in the repository.

Run the image in Docker:

> docker run -p 3001:3000 -d curso-kind-nodejs:0.0.1

This command will run a container from the curso-kind-nodejs:0.0.1 image and map port 3000 of the container to port 3001 on the host.

Create a KIND cluster:

> kind create cluster

This command will create a local KIND cluster on your machine.

Load the image into KIND:

> kind load docker-image curso-kind-nodejs:0.0.1

This command will load the Docker image curso-kind-nodejs:0.0.1 into the KIND cluster so that it can be used by Kubernetes.

Deploy the image within Kubernetes:

> kubectl expose deploy app-web --port 3000

This command will deploy the app-web image in Kubernetes and expose port 3000.

Create the ingress:

kubectl apply -f ingress.yml

This command will create the ingress using the ingress.yml configuration file.

Congratulations! You have now launched and set up the application in your Docker and Kubernetes environment using KIND.

Contact
If you have any questions or encounter any issues, you can contact the support team at robertfrcoding@gmail.com
