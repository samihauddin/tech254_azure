### Creating SSH Key on Azure

**Step 1:** Generate an SSH Key pair locally 
- Navigate to your GitBash terminal 
- Enter your .ssh folder `cd .ssh`
- Generate a new key pair: `ssh-keygen -t rsa -b 4096 -C "samihauddin@live.co.uk"`
- Press Enter and name the key appropriately

#### Uploading the Public key to Azure Portal 

**Step 2:** Login to Azure Portal
- https://portal.azure.com/signin/index/

**Step 3:** Navigate to the SSH Keys Section 

![alt text](Images/3.png)

**Step 4:** Add SSH Key
- Select `Create SSH Key`
- Enter your Key pair name
- Select `Upload existing public key`
- Copy and paste your public SSH that you created in step 1

![alt text](Images/4.png)

**Step 5:** Create a Tag
- Name `Owner`
- Value `Your Name`

**Step 6:** Review and Create
- Review input and then select create

![alt text](Images/6.png)

### Creating a VPC on Azure

**Step 1:** Login to Azure Portal
- https://portal.azure.com/signin/index/

**Step 2:** Navigate to Virtual Network
- In the top search bar enter Virtual Network

![alt text](Images/7.png)

**Step 3:** Configure VNet Settings

- Select `Create`
- Enter a Virtual network name
- Region: `Europe UK South`

![alt text](Images/8.png)

**Security**
- Leave as default

**IP addresses**
- Enter the IP address range for your VNet `10.0.0.0/16`
- Create a public subnet
- Create a private subnet

![alt text](Images/9.png)
![alt text](Images/10.png)

**Create a Tag**
- Name `Owner`
- Value `Your Name`

**Review and Create**
- Review your configurations to ensure everything is correct.
- Click on the "Review + create" button to validate your settings.
- After validation passes, click on the "Create" button to create your VNet.

![alt text](Images/11.png)

**Successful output**

![alt text](Images/12.png)

### Creating a VM on Azure

**Step 1:** Login to Azure Portal
- https://portal.azure.com/signin/index/

**Step 2:** Navigate to Virtual Machine
- In the top search bar enter Virtual Machine
- Select `Create`
- Select `Azure Virtual Machine`

![alt text](Images/13.png)

**Step 3:** Project Details
- Name appropriately 
- Select `Availibilty Zone`
- Select `Zone 1`

![alt text](Images/14.png)

**Step 4:** Security type

`Ubuntu Pro 10.04 LTS x64 Gen2` <br>
`Standard`

![alt text](Images/15.png)

**Step 5:** VM size 
- Click `see all sizes`
- Search `B1s` and select

![alt text](Images/16.png)

**Step 6:** Administrator account 
- Change default username to `adminuser`
- Select `Use existing key stored in Azure`
- Select your key name

![alt text](Images/17.png)

**Step 7:** Inbound port rules
- Select HTTP (80) and SSH (22)

![alt text](Images/18.png)

**Step 8:** OS Disk
- Check Delete with VM

**Step 9:** Networking 
- Select your Virtual Network
- Select `Public Subnet`
- NIC network security group `Basic`
- Check Delete Public IP and NIC when VM is deleted

![alt text](Images/19.png)
![alt text](Images/20.png)

Step 10: Management and Monitoring
- Leave as default

Step 11: Advanced
- Check `Enable User data`
- Enter your script

![alt text](Images/21.png)

**Step 12:** Create a Tag
- Name `Owner`
- Value `Your Name`

**Step 13:** Review and Create
- Review your configurations to ensure everything is correct.
- Click on the "Review + create" button to validate your settings.
- After validation passes, click on the "Create" button to create your Virtual Machine.

![alt text](Images/22.png)

**Successful output**
- You can now copy and paste your public IP address 

![alt text](Images/23.png)