# Hello World Node.js

This is simple Node.js application.

## How to deploy a simple Node.js application

### to a web app in Azure App Service by using Git

Please see below for the details.

[Create a Node.js web app in Azure App Service | Microsoft Azure](https://azure.microsoft.com/en-us/documentation/articles/web-sites-nodejs-develop-deploy-mac/)

### to a web app in Azure App Service by using Visual Studio Online

(At October 20, 2015)

1. Using Git. This is the easiest way.
	1. Create the build definition.
	2. Select the [Empty], then click the [OK].
	3. Click [+ Add build step…], then click [Utility].
	4. Click [Command Line]'s [Add] twice, then click [Close].
	5. Input 1st [Command Line],  
	`Tool`: `git`  
	`Arguments`: `remote add azure https://[username]:[password]@[sitename].scm.azurewebsites.net:443/[sitename].git`
	6. Input 2nd [Command Line],  
	`Tool`:`git`  
	`Arguments`:`push azure master`
	7. Select the continuous integration (CI) trigger and specify the code you want to build.
	8. Save the definition.
	9. Queue your new definition to make sure it works.
