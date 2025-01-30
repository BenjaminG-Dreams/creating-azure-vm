<p align="center">
</p>
<p align="center">
<img src="https://www.imagar.com/wp-content/uploads/2018/06/azure.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>How to Setup VMs and a Virtual Network in Azure</h1>
This is an simple online tutorial to teach beginners how to create multiple virtual machines and virtual network in Azure. After creating the virtual network, we will observe the network topology through Newtork Watcher.<br />

<h2>Pre-requisites </h2>

- [Setup a Subscription and a Resource in Azure for Beginner Labs](https://github.com/BenjaminG-Dreams/setup-azure-sub-and-resource)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Compute/Networking)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Linux (ubuntu server 20.04)

<h2>Steps</h2>

- Step 1: Create a new Resource Group within the Azure Portal
- Step 2: Create a Windows 10 virtual machine
- Step 3: Create a Ubuntu Server virtual machine
- Step 4: Observe Your Virtual Network within Network Watcher
- Step 5: Clean up the resource group


<h2>Virtual Machine and Network Creation</h2>

<p>
<img src="https://i.imgur.com/pXKn1Uq.png"/>
</p>
<p>
First, log into the Azure portal by typing in https://portal.azure.com/. If you do not have a account with Azure, please look at pre-requisites to create an account and get accustumed to the application.
</p>
<br />

![Screenshot 2025-01-28 203522](https://github.com/user-attachments/assets/e4d75f47-1d7d-4ae3-ba44-6f3d14508b79)

<p>
Now, navigate to the Resource Group page by either typing the name in the search bar or choosing the button at the homepage of the Azure portal. Secondly, create a new resource group and name it whatever you would like. For this tutorial I will be using "RG-2". After this select the region that is closest to you, I will be using "east US 2". When finished, press "Review + create" button at the bottom left of the screen. Lastly, press create.
</p>
<br />

![Screenshot 2025-01-28 224634](https://github.com/user-attachments/assets/18d249b5-7120-4deb-80b8-bc94da1e0b13)

![Screenshot 2025-01-29 191446](https://github.com/user-attachments/assets/b203fcfb-3075-4c44-aa52-75cdf7a4587b)

<p>
Create a Virtual Machine by going to the page by typing the name in the search bar or pressing the button on the homepage of the portal. Then you will press create a VM and will be redirected to the page in the photo. Double check that the subscription is set to your subscription and choose the resource group that you created. You will then name the resource group to your liking. This tutorial we will be using "VM1". After naming the virtual machine, we will select the same region that you chose for the resource group. We will use that same region throughout this lab including the next virtual machine we will create after this one. Select Windows 10 Pro as the image for this VM.
</p>
<br />

![Screenshot 2025-01-29 191547](https://github.com/user-attachments/assets/f1725635-b558-4627-aa8d-232aaf479618)

<p>
After that, select the vcpus and RAM size of the VM. Select the one with at least 2 vcpus and at least 8 GB of RAM so the virtual machine is not slow. Now you will create a username and password which I recommend writing down for this tutorial just in case. You will then hit the checkbox at the bottom of the screen and then press next button until you reach the networking section. 
</p>
<br />

![Screenshot 2025-01-29 191650](https://github.com/user-attachments/assets/36185b71-3ae5-4ae9-add0-8b339f6133c0)

![Screenshot 2025-01-29 191806](https://github.com/user-attachments/assets/08b20820-7dae-43ad-a12b-f746b891c259)

<p>
The VM will create its own virtual network, subnet and public IP. Leave these options alone and press "Review + Create" at the bottom. Finalize the VM by pressing create afterwards.
</p>
<br />

![Screenshot 2025-01-28 224634](https://github.com/user-attachments/assets/52b715e6-3236-4048-9878-e1fed26b3d5b)

<p>
When the VM is finished deploying, you will go back onto the VM page to create another VM.
</p>
<br />

![Screenshot 2025-01-29 192042](https://github.com/user-attachments/assets/00611b30-1da0-47e3-963f-3ff2978ea013)

<p>
We will now set the resource group to the same one as the Windows 10 VM and make sure the subscription is the same as well. We'll name this VM2 and make sure the region is the exact same as the other VM. Instead of Windows 10, we'll select Ubuntu Server 22.04 LTS as your image and check the x64 architecture.
</p>
<br />

![Screenshot 2025-01-29 192042](https://github.com/user-attachments/assets/fcf1b48d-3329-418c-befe-98fbef53f775)

<p>
Set the size as the same as the first VM we created. Choose password for authentication type and create your username and password. For simplicity of this tutorial, we'll use the same one as the first VM. Finally, hit next button until you arrive at the networking section.
</p>
<br />

![Screenshot 2025-01-29 193007](https://github.com/user-attachments/assets/a3ba43b3-0e3d-4fb2-9d78-b04f74cbc5dd)

<p>
Select the asame Vnet that the Windows VM created. This should be deafult, but if it is different make sure to change it. Afterwards, just make sure everything is default as well and then hit the "Review + Create" button. Lastly, finish off this VM by pressing "Create".

![Screenshot 2025-01-29 191806](https://github.com/user-attachments/assets/584a4a13-ddfb-4732-86b9-514b9c2a5474)

</p>
<br />
