Using a VM to run the server was as easy as sharing a folder between the guest and host OS and running the code.
Running the projects using kind was a bit more difficult and included the steps:
1. creating a deployment yaml file
2. creating a registry secret
3. creating a service in order to expose the service pod
4. inspecting the service to find the server IP address
5. creating a configmap of the server ip address and utilizing it as an env var in the client code 

While kubernetes may have a steeper learning curve I believe the containerized kubernetes methodology is preferable to the VM implementation in virtually every aspect.
1. ease of use: once you familiarize youself with kubectl syntax it becomes very intuitive and easy to deploy and customize applications while in a VM you must do everything manually
2. scalability: it is very easy to scale applications using kubernetes
3. protection mechanisms: including rollout methodologies, health checks, replication colntrollers and services are all built in and easy to use in kubernetes
