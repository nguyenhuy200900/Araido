**What’s in this document?**

* What tools need to be installed?
* how to deploy? 

**BOT Framework Composer**

If you are using the [Bot Framework Composer](https://docs.microsoft.com/en-us/composer/install-composer?tabs=windows) to develop, please find the setup documentation on this [link](https://www.dropbox.com/s/2fubc6po6i97iwb/Bot%20Framework%20Composer%20Set%20Up%20Keys.docx?dl=0).

For further codebase development, please install [the 3.1 .Net core SDK](https://dotnet.microsoft.com/download) and the [Bot Framework Composer](https://docs.microsoft.com/en-us/composer/install-composer?tabs=windows)

**Local Develop**

**Prerequisites:**

* Newest version of NodeJS installed.
* VS Code or any code editor application install.
* A working Azure account with company subscription.



Install the Git repository of dsoa-support-chatbot master branch.

Or if you have access to the Azure portal [Microsoft Azure](portal.azure.com), from the Web App Bot choose the option ‘Dowload bot source code’:

Extract the zip file and open it in VS Code or any code editor application.

Install botbuilder: 

`npm install botbuilder --save`

Install restify (In this part, if you run to any errors, check for a version of Python, Anaconda recommended): 

`npm install restify --save` 

Install type for restify:

`npm install @types/restify --save`

Install botbuider-ai: 

`npm install botbuider-ai --save`

 

**Prepare for deployment**

Login to Azure

`az login`

Set the subscription

`az account set --subscription “<azure-subscription-id>”`

If you aren't sure which subscription to use for deploying the bot, you can view the list of subscriptions for your account by using `az account list` command.

 

**Deploy code to Azure**

`az webapp deployment source config-zip --resource-group "<resource-group-name>" --name "<name-of-web-app>" --src "<project-zip-path>"`

| Option | Description |
| ------ | ------ |
| resource-group | The name of the Azure resource group that contains your bot. |
| name | Name of the Web App you used earlier. | 
| src | The path to the zipped project file you created. | 


Or, you can publish the code locally using your VSCode Azure Extensions.
