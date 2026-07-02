# az_204
Azure Container Registery , AKS , Azure Container Instance .



Create Web App from Docker Container in Azure


Lab Diagram 

![alt text](image.png)


Scenario for the lab.

![alt text](image-1.png)


GitHub URL where the DockerFile is present 
https://github.com/ACloudGuru-Resources/content-AZ-104-Microsoft-Azure-Administrator/tree/js-docker


Create a New Container Registry

az acr create --resource-group $RG --name $ACR --sku Basic --admin-enabled true

Build an Image and Push to ACR

git clone --branch js-docker https://github.com/ACloudGuru-Resources/content-AZ-104-Microsoft-Azure-Administrator.git ./js-docker

cd js-docker/

Build and push the image to Azure Container Registry using ACR Tasks and the Dockerfile provided (<IMAGE_NAME> can be anything you like e.g. js-docker:v1):

az acr build --image dj-shashi:v1 --registry $ACR --file Dockerfile .


As we can see the image is created In the ACR.

![alt text](image-2.png)


From here we can deployed this image in the web app , Azure container image , AKS cluster.

Create and Deploy a New Web App

-> while creating the web to host the image select container in the publish options.

![alt text](image-3.png)


In the container setting select this options.
![alt text](image-4.png)

We app overview page created with container.

![alt text](image-5.png)

The Web app Url is working.

![alt text](image-6.png)






![Uploading image.png…]()
>>>>>>> 53ef858ff1bd884f89b1076b2b2e78171551612e
