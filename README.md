# Azure_DevOps_ArgoCD_CI 

1. In the dev.azure.com -> Goto Repos -> Files -> Import -> Clone URL - `https://github.com/dockersamples/example-voting-app.git`


2. Azure DevOps makes the default branch alphabetically So -> Reops -> Branches -> Select the Branch - main -> 3 dots and select Set as the default branch 


3. Now goto portal.azure.com -> Resouce group -> Create -> Name - azurecicd -> Click on Review + create


4. In portal.azure.com -> Container registry -> Create -> Resouce group - azurecicd -> Registry name - pavanazurecicd -> Click on Review + create


5. Goto dev.azure.com -> Pipelines -> Pipelines -> Create pipeline -> Select Azure Repos Git -> Select the repo -> Click on Docker (Build and push an image to Azure Container Registry) -> Select the subscription -> Container registry - pavanazurecicd -> Click on Validate and configure


6. Now goto portal.azure.com -> Virtual machines -> Create -> Resouce group - azurecicd -> Virtual mahine name - agentpool-pavan -> Click on Review + create


7. Go to dev.azure.com -> Project Settings -> Agent pools -> Click Add pool -> Pool type - Self-hosted -> Name - Azure-Pool-CICD -> Enable Grant access permission to all pipelines -> Click on Create -> Select the pool created -> Click on New agent -> Select Linux 

Exceute the commands by logging into the VM created in Step 6. 

Also install docker on the agent

sudo apt install docker.io

sudo usermod -aG docker azureuser

sudo systemctl restart docker


8. Now goto dev.azure.com and run the pipeline 


9. Similarity create another pipleline for Result-App following Step 5.



