---
services: cosmos-db
platforms: nodejs
author: ryancrawcour
---

# Web application development with Node.js and Express using Azure Cosmos DB
This sample shows you how to use the Azure Cosmos DB service to store and access data from a Node.js Express application hosted on Azure Websites. 

![My ToDo List Node.js application](./media/image1.png)

For a complete end-to-end walk-through of creating this application, please refer to the [full tutorial on the Azure documentation page](https://docs.microsoft.com/azure/cosmos-db/sql-api-nodejs-application)

## Running this sample
1. Before you can run this sample, you must have the following perquisites:
	- An active Azure Cosmos DB account - If you don't have an account, refer to the [Create an Azure Cosmos DB account](https://docs.microsoft.com/azure/cosmos-db/sql-api-nodejs-application#_Toc395637761) article.
	- [Node.js](https://nodejs.org/en/) version v0.10.29 or higher.
	- [Express generator](http://expressjs.com/starter/generator.html) (you can install this via npm install express-generator -g)
	- [Git](http://git-scm.com/).

2. Clone this repository, or download the zip file.

3. Retrieve the URI and PRIMARY KEY (or SECONDARY KEY) values from the Keys blade of your Azure Cosmos DB account in the Azure portal. For more information on obtaining endpoint & keys for your Azure Cosmos DB account refer to [How to manage an Azure Cosmos DB account](https://docs.microsoft.com/azure/cosmos-db/manage-account).

	If you don't have an account, see [Create an Azure Cosmos DB database account](https://docs.microsoft.com/azure/cosmos-db/sql-api-nodejs-application#_Toc395637761) to set one up.

4. In the **config.js** file, located in the **src** folder, find **config.host** and **config.authKey** and replace the placeholder values with the values obtained for your account.

	<add key="endpoint" value="~enter URI for your Azure Cosmos DB Account, from Azure portal~" /> 
	<add key="authKey" value="~enter either Primary or Secondary key for your Azure Cosmos DB account, from Azure portal~" /> 

5. Install the dependencies by opening a terminal, navigating to the directory in which the sample was installed, and running **npm install**. 

6. In the terminal, run **npm start** to start your start your node application. 

7. Launch a browser and navigate to **http://127.0.0.1:3000/**
![My ToDo List Node.js application](./media/run-1.png)

## Deploy this sample to Azure

1. If you haven't already, enable a git repository for your Azure Website. You can find instructions on how to do this [here](https://azure.microsoft.com/en-us/documentation/articles/web-sites-publish-source-control-git/#step4).

2. Add your Azure Website as a git remote.

		git remote add azure https://username@your-website.scm.azurewebsites.net:443/your-website.git

3. Deploy by pushing to the remote.

		git push azure master

4. In a few seconds, git will finish publishing your web application and launch a browser where you can see your handy work running in Azure!

## About the code
The code included in this sample is intended to get you going with a simple Node.js Express application that connects to Azure Cosmos DB with the express intent of demonstrating how to interact with Azure Cosmos DB using the [documentdb npm package](https://www.npmjs.com/package/documentdb). It is not intended to be a set of best practices on how to build scalable enterprise grade web applications. This is beyond the scope of this quick start sample. 

## More information

- [Azure Cosmos DB Documentation](https://docs.microsoft.com/azure/cosmos-db/)
- [Azure Cosmos DB Node SDK](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-node)
- [Azure Cosmos DB Node SDK Reference Documentation](http://azure.github.io/azure-documentdb-node/DocumentClient.html)
