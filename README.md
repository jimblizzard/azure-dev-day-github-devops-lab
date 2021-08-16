# azuredevday

GH and AzDO Lab

## Create an Azure DevOps Starter Project

1. Sign into the Microsoft Azure Portal
1. In the search bar, type **DevOps Starter** and press **Return**
1. Click on **+ Create**
1. Make sure that it's going to set up the DevOps starter with Github. If it isn't, click on the **change settings here** link.
1. Select the **Node.js** box.
1. Click **Next: Framework >**
1. Select the **Express.js** box. There's no need to add a database. 
1. Click **Next: Service >**
1. Select the **Windows Web App** box. 
1. Select **Next: Create >**
1. Click **Authorize** to a
1. Enter your GitHub Organization, Repository, Azure SubScription, Web app name, and Location. 
1. Click **Review + Create**

    Note: It will take a few minutes to create the Azure and GitHub resources. Go grab a soda or some coffee. 

1. Once the deployment completes, click on **Go to resource** to view the deployment. 

## View your DevOps Starter project and create a Deployment slot

1. Click on **Authorize** to allow Azure to access your GitHub account to view the latest workflow execution and status of jobs
1. CLick on **Authorize** to finish connecting your GitHub account
1. From here you can see the GitHub workflow and the Azure resources that were created. 
1. Click on your App Service name to go to the App Service definition in the Azure portal.
1. Click on **Deployment slots** 
1. Click on **+ Add Slot** and name the slot "pre-prod" and choose Clone settings from: **{your production slot name}**
1. Click **Add**. It will take a minute or so to create the pre-prod slot. Once it finishes, click **Close** at the boottom of that window.

    You should now see two slots, the production slot and the new, pre-prod slot.

## Update your GitHub workflow to add an action to swap the slots
1. Open a new tab and browse to your GitHub account. 
1. Click on **Repositories** to view your repositories. 
1. Open your new repository by clicking on its name. It is named the same as the name of the App Service you created. 
1. Click on **.github/workflows** then **devops-starter-workflow.yml** to see the CICD pipeline that was created by the DevOps Starter project. 

    The workflow contains three jobs. **build**, **Deploy**, and **FunctionalTests**.
