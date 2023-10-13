# Azure Function App to Read and Write data to Blob-Storage

An Azure function app that reads and writes data to a blob (txt file) in Azure blob storage in Python.

This is a simple function app that executes every 15 minutes based on a <a href="https://github.com/Ndarugaa/Azure-Function-App-to-Read-and-Write-to-Blob-Storage/tree/main/TimerTrigger1">Timer Trigger </a>. <br>Each time the function app runs, a random number between 1 - 10 is generated <strong>only once</strong>. The number is then logged to the text file along with the time it was generated and a random word.
The Function checks if a number exists and generates it if it doesn't exist otherwise it skips the number.


## Prerequisites
<ul>
  <li>Azure Account</li>
  <li><a href="https://code.visualstudio.com/download">Visual Studio Code </a> with <a href="https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-node-azure-pack">Azure Extension installed</a></li>
  <li>Connection String</li>
  <li>Container Name</li>
  <li>Blob Name</li>
</ul>

## Cloning the repository
To clone the repository, open the terminal and paste the code below:
```
git clone https://github.com/Ndarugaa/Azure-Function-App-to-Read-and-Write-to-Blob-Storage.git
```
Open the cloned repository folder with Visual Studio code.

#### 1. Azure Account
Login to your Azure Account
> 1. Go to https://portal.azure.com/#home
> 2. On the Left menu, Under <strong>Storage accounts</strong>
> 3. Select an existing or create a new Storage Account.

Creating a storage account
![Recording 2023-10-13 033015](https://github.com/Ndarugaa/Azure-Function-App-to-Read-and-Write-to-Blob-Storage/assets/68260816/08403590-2840-4a66-a768-7020160fa70e)


#### 2. Connection String
The connection String is important for connecting your function app to the blob storage
> 1. On the <strong>Storage Accounts Menu</strong>
> 2. Under <strong>Security + Networking</strong>, Select <strong>Access Keys</strong>

> ![image](https://github.com/Ndarugaa/Azure-Function-App-to-Read-and-Write-to-Blob-Storage/assets/68260816/f8c7debc-698a-47c4-9229-7a8cce484596)

> 3.  Under `Key1` or `Key2` copy any of the `connection strings`

>   ![image](https://github.com/Ndarugaa/Azure-Function-App-to-Read-and-Write-to-Blob-Storage/assets/68260816/755cd3b9-ee02-4bde-9495-6c4f50b680b8)

> 4. Paste the connection string to the `__init__.py` file, in the `connection string` variable in `line 16`

#### 3. Blob Storage - Container Name & Blob-name
> 1. In the `__init__.py` file
> 2. In line 17 change the `container name` variable to your desired container name.
> 3. In line 18, Change the `blob name` variable to the desired blob name
<h6><strong>Note: </strong>The following characters are not allowed in container names: uppercase letters, spaces, and special characters such as #, %, and &</h6>

![connection-string](https://github.com/Ndarugaa/Azure-Function-App-to-Read-and-Write-to-Blob-Storage/assets/68260816/4c2cb247-47ae-4f30-9a04-f25c3a0dc7df)

## Execution

Ensure that you have the `Azure extension` installed. Once VScode has opened, click on the `Azure icon`.

On the Azure menu that appears, Right click on `Function App` and `Create a Function App in Azure`

Pop-up questions to create the function appear at the top of the open Visual Studio code window.

Once the function app has been successfully created, Under the Workspace submenu, click on the function app `icon` and then click `Deploy to Function app`.

![image](https://github.com/Ndarugaa/Azure-Function-App-to-Read-and-Write-to-Blob-Storage/assets/68260816/796f367a-53dc-4737-879f-84a18baff65b)

## Follow-up
To check the status of your function app, open the `Azure portal`, 

under Function App, click on your Function App name. 

Open the `TimerTrigger`

In the Function App menu that appears, click on `Monitor` 

Notice that the function executes after every minute. <a href="https://github.com/Ndarugaa/Azure-Function-App-to-Read-and-Write-to-Blob-Storage/tree/main/TimerTrigger1">Read More Here </a>



