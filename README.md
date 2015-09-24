---
services: documentdb
platforms: node
author: ryancrawcour
---

# Web application development with Node.js and Express using DocumentDB
This sample shows you how to use the Microsoft Azure DocumentDB service to store and access data from a Node.js Express application hosted on Azure Websites. 

![My ToDo List Node.js application](./media/image1.png)

For a complete end-to-end walk-through of creating this application, please refer to the [full tutorial on the Azure documentation page](https://azure.microsoft.com/en-us/documentation/articles/documentdb-nodejs-application/)

## Running this sample
1. Before you can run this sample, you must have the following perquisites:
	- An active Azure DocumentDB account - If you don't have an account, refer to the [Create a DocumentDB account](https://azure.microsoft.com/en-us/documentation/articles/documentdb-create-account/) article.
	- [Node.js](https://nodejs.org/en/) version v0.10.29 or higher.
	- [Express generator](http://expressjs.com/starter/generator.html) (you can install this via npm install express-generator -g)
	- [Git](http://git-scm.com/).

2. Clone this repository, or download the zip file.

3. Retrieve the URI and PRIMARY KEY (or SECONDARY KEY) values from the Keys blade of your DocumentDB account in the Azure Preview portal. For more information on obtaining endpoint & keys for your DocumentDB account refer to [How to manage a DocumentDB account](https://azure.microsoft.com/en-us/documentation/articles/documentdb-manage-account/#keys)

	If you don't have an account, see [Create a DocumentDB database account](https://azure.microsoft.com/en-us/documentation/articles/documentdb-create-account/) to set one up.

4. In the **config.js** file, located in the **src** folder, find **config.host** and **config.authKey** and replace the placeholder values with the values obtained for your account.

	<add key="endpoint" value="~enter URI for your DocumentDB Account, from Azure Preview portal~" /> 
	<add key="authKey" value="~enter either Primary or Secondary key for your DocumentDB Account, from Azure Preview portal~" /> 
5. Run **npm start** in a terminal to start your start your node application, and launch a browser and navigate to **http://127.0.0.1:3000/**
![My ToDo List Node.js application](./media/run-1.png)

## Deploy this sample to Azure

1. If you haven't already, enable a git repository for your Azure Website. You can find instructions on how to do this [here](https://azure.microsoft.com/en-us/documentation/articles/web-sites-publish-source-control-git/#step4).

2. Add your Azure Website as a git remote.

		git remote add azure https://username@your-azure-website.scm.azurewebsites.net:443/your-azure-website.git

3. Deploy by pushing to the remote.

		git push azure master

4. In a few seconds, git will finish publishing your web application and launch a browser where you can see your handy work running in Azure!

## About the code
The code included in this sample is intended to get you going with a simple Node.js Express application that connects to Azure DocumentDB with the express intent of demonstrating how to interact with DocumentDB using the [documentdb npm package](https://www.npmjs.com/package/documentdb). It is not intended to be a set of best practices on how to build scalable enterprise grade web applications. This is beyond the scope of this quick start sample. 

## More information

- [Azure DocumentDB Documentation](https://azure.microsoft.com/en-us/documentation/services/documentdb/)
- [Azure DocumentDB Node SDK](https://www.npmjs.com/package/documentdb)
- [Azure DocumentDB Node SDK Reference Documentation](http://azure.github.io/azure-documentdb-node/)
