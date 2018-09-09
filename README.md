# Croc Hunter - The game!

For those that have dreamt to hunt crocs

# Usage
Basic go webserver to demonstrate example CI/CD pipeline using Kubernetes 

# Deploy using Jenkins Chart and Helm
[![Demo Pipeline](https://img.youtube.com/vi/NVoln4HdZOY/0.jpg)](https://youtu.be/NVoln4HdZOY "Demo Pipeline")

# How to setup the Jenkins infrastructure 
[![Jenkins Setup](https://img.youtube.com/vi/eMOzF_xAm7w/0.jpg)](https://youtu.be/eMOzF_xAm7w "Jenkins Setup")
* See DEMO.md for steps


# Set up steps
1. Step 1, Modify jenkins-values.yaml 
2. Setp 2, Run command: helm install stable/jenkins -f jenkins-values.yaml --name my-jenkins --namespace jenkins-blue
3. Step 3, Get jenkins password: printf $(kubectl get secret --namespace jenkins-blue my-jenkins -o jsonpath="{.data.jenkins-admin-password}" | base64 --decode); echo
