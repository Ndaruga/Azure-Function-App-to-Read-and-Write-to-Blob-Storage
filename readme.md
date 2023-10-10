# Azure Function App to Read and Write data to Blob-Storage

An Azure function app that reads and writes data to a blob (txt file) in Azure blob storage in python.

This is a simple function app that executes every 15 minutes based on a <a href="https://github.com/Ndarugaa/Azure-Function-App-to-Read-and-Write-to-Blob-Storage/tree/main/TimerTrigger1">Timer Trigger </a>. <br>Each time the function app runs, a random number between 1 - 10 is generated. The number is then logged to the text file along with the time it was generated and a random word.

## Prerequisites
<ul>
  <li>Azure Account</li>
  <li>Connection String</li>
  <li>Container Name</li>
  <li>Blob Name</li>
</ul>

## How it works
#### 1. Azure Account
Login to your Azure Account
> 1. Go to https://portal.azure.com/#home
> 2. On the Left menu, Under <strong>Storage accounts</strong>
> 3. Select an existing or create a new Storage Account.

#### 2. Connection String
The connection String is important for connecting your function app to the blob storage
> 1. On the <strong>Storage Accounts Menu</strong>
> 2. Under <strong>Security + Networking</strong>, Select <strong>Access Keys</strong>

> ![image](https://github.com/Ndarugaa/Azure-Function-App-to-Read-and-Write-to-Blob-Storage/assets/68260816/f8c7debc-698a-47c4-9229-7a8cce484596)

> 3.  Under `Key1` or `Key2` copy any of the `connection strings`

>   ![image](https://github.com/Ndarugaa/Azure-Function-App-to-Read-and-Write-to-Blob-Storage/assets/68260816/755cd3b9-ee02-4bde-9495-6c4f50b680b8)

> 4. Paste the connection string to the `__init__.py` file, in the `connection string` variable in `line 16`

#### 3. Blob Storage - Container Name
> 1. In the `__init__.py` file
> 2. In line 17 change the `container name` variable to your desired container name.
> 3. In line 18, Change the `blob name` variable to the desired blob name
