---
page_type: sample
languages:
- java
products:
- azure
extensions:
  services: Kubernetescluster
  platforms: java
---

# Getting Started with Kubernetescluster - Deploy Image From Container Registry To Kubernetes - in Java #


  Azure Container Registry sample for deploying a container image to Azure Container Service with Kubernetes orchestration.
   - Create an Azure Container Registry to be used for holding the Docker images
   - If a local Docker engine cannot be found, create a Linux virtual machine that will host a Docker engine to be used for this sample
   - Use Docker Java to create a Docker client that will push/pull an image to/from Azure Container Registry
   - Pull a test image from the public Docker repo (tomcat:8) to be used as a sample for pushing/pulling to/from an Azure Container Registry
   - Create a new Docker container from an image that was pulled from Azure Container Registry
   - Create a SSH private/public key to be used when creating a container service
   - Create an Azure Container Service (AKS) resource
   - Log in via the SSH client and download the Kubernetes config
   - Create a Kubernetes client using the Kubernetes config file downloaded from one of the virtual machine managers
   - Create a Kubernetes namespace
   - Create a Kubernetes secret of type "docker-registry" using the Azure Container Registry credentials from above
   - Create a Kubernetes replication controller using a container image from the Azure private registry from above and a load balancer service that will expose the app to the world
 

## Running this Sample ##

To run this sample:

See [DefaultAzureCredential](https://github.com/Azure/azure-sdk-for-java/tree/main/sdk/identity/azure-identity#defaultazurecredential) and prepare the authentication works best for you. For more details on authentication, please refer to [AUTH.md](https://github.com/Azure/azure-sdk-for-java/blob/main/sdk/resourcemanager/docs/AUTH.md).

    git clone https://github.com/Azure-Samples/aks-java-deploy-image-from-acr-to-kubernetes.git

    cd aks-java-deploy-image-from-acr-to-kubernetes

    mvn clean compile exec:java

## More information ##

For general documentation as well as quickstarts on how to use Azure Management Libraries for Java, please see [here](https://aka.ms/azsdk/java/mgmt).

Start to develop applications with Java on Azure [here](http://azure.com/java).

If you don't have a Microsoft Azure subscription you can get a FREE trial account [here](http://go.microsoft.com/fwlink/?LinkId=330212).

---

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.