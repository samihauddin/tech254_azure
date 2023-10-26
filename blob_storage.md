### What is Azure Blob Storage?

Azure Blob Storage is Microsoft Azure's object storage solution for the cloud.

Azure Blob Storage is highly scalable and can store and serve large amounts of unstructured data.

It is commonly used for backups, archiving, data lakes, IoT data, and much more.

### 3 Types of Blob Storage?
- Block blobs
- Page blobs
- Append blobs

### Blob Storage 
- You can store anything in blob storage such as Videos, pictures 
- It needs a storage account, you cannot create a blob without one. 
- A blob storage is unorganised and blobs go inside a container.
- In order to organise the containers, you will need to create a new container.
- The storage account belongs inside our resource groups.

### Access Tiers 

- Access tiers in Azure Blob Storage refer to the different storage classes that allow you to store your data at different levels of durability and access costs. 

There are 3 different access tiers: <br>
- **Hot Access Tier:** This tier is optimized for frequently accessed data. <br>
- **Cool Access Tier:** This tier is optimized for infrequently accessed data. <br>
- **Archival Tier:** This is used when it is hardly ever accessed. 


1. SHH into Gitbash terminal 
2. Change from Root to User 
```
cd /
```
3. Then enter app folder
```
cd repo
ls
cd app
```

4. Check if node is running
```
ls
pm2 list
pm2 start app.js
node app.js
```

### How to stop Node.js from running

```
# list all the processes running
ps aux 

# lists only node processes
ps aux | grep node

# In order to kill node we need to kill pm2 as this keeps restarting node 
ps aux | grep pm2
sudo kill 17307
```

### How to set up Azure CLI

**Step 1:** Install Azure CLI
- Navigate to Azure CLI Installation Guide.
https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-linux?pivots=apt
- Select `Install Linux`
- Navigate to `Option 1: Install with one command`
- Copy and paste the command into the GitBash terminal
```
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
```

**Step 2:** Login to Your Azure Account

```
az login
```
**Step 3:** Follow the steps in the terminal 
- Copy and paste the URL in a browser
- Enter the code given from the terminal
- Login through your Microsoft Azure email and password.
- Press continue

![alt text](Images/cli.png)
![alt text](Images/cli2.png)

### Successful output 

![alt text](Images/cli3.png)