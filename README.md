<p align="center">
<img width="542" height="303" alt="image" src="https://github.com/user-attachments/assets/d84b1060-f919-443b-8b7f-1f95040b958e" />

</p>

<h1>Configuring a Virtual machine and Remote desktop (RDP) access</h1>
This tutorial outlines the system and usage surrounding Remote Desktop protocol usage.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 11</b> (25H2)

<h2>List of Prerequisites</h2>

- Internet Connection
- Remote Desktop Connection (Usually preinstalled Software within Windows)
- Microsoft Azure Account for Virtual machine deployment
- A pre setup Azure account (Free or paid) This lesson is done on a FREE account.
- https://azure.microsoft.com/

<h2>Installation Steps</h2>
First start off by creating a resource group. A resource group is basically just a folder used to store and organize your work/servers.
<p><img width="1122" height="330" alt="image" src="https://github.com/user-attachments/assets/b3c9832a-928e-47c0-992a-02bf0087fba8" /></p>


Name it what you please click review and then create.
<p><img width="856" height="827" alt="image" src="https://github.com/user-attachments/assets/d9db56ae-9d33-4de7-bbbb-f430e31889c6" />
</p>

Once created you will see it show up within the "Resource Groups" Tab. We named ours rdp-portfolio

<p><img width="1660" height="351" alt="image" src="https://github.com/user-attachments/assets/cb77b204-e158-4a61-85d0-91f07f9d697b" />
</p>

Then you will navigate to "Virtual Machines" which can be simply typed in the search bar at the top or along the side in the Directory.
<p><img width="1101" height="292" alt="image" src="https://github.com/user-attachments/assets/394082dd-c3b0-4fe6-98dc-05fcf275e700" />
</p>

Now that we have navigated over to the virtual machines tab, lets take a look at how to properly set up a virtual machine within your resource group.

First click create and select "Virtual Machine"
<p><img width="368" height="173" alt="image" src="https://github.com/user-attachments/assets/7fa05527-3d67-4b31-88dd-8e5ec15bd4ce" />
</p>

Make sure to select the resource group you would like to organize the VM into. As you can see I have multiple resource groups for other projects and virtual machines I work with so organization is key. Remember we named ours rdp-portfolio so thats the one I will select
<p><img width="750" height="259" alt="image" src="https://github.com/user-attachments/assets/84927cf2-1d22-4a4d-ab67-0b4c45beedc4" />
</p>

Next you will name your Virtual machine (Keep it related for organization purposes) and select a "Region" youd like to deploy your virtual machine from.
<p><img width="766" height="563" alt="image" src="https://github.com/user-attachments/assets/23565cd1-3274-4dd1-9ec3-403497d28af1" />
</p>

Now is when you decide which OS (Operating system) you will be using for your Virtual Machine. Within Azure there are many to pick from for a multitude of uses, for this lesson we will simply use a windows 10 OS.
<p><img width="806" height="494" alt="image" src="https://github.com/user-attachments/assets/93c9eee3-c4e3-4451-9d9e-3363d2874980" />
</p>
<p><img width="793" height="56" alt="image" src="https://github.com/user-attachments/assets/3054fb66-8c9a-4ac7-8e03-a3c984927c8f" />
</p>

When you create a Virtual Machine (VM) in Microsoft Azure, the “size” you choose is basically the hardware profile of that VM. It determines how powerful (and expensive) your VM will be.
<p><img width="802" height="277" alt="image" src="https://github.com/user-attachments/assets/f4ba93a9-b2b7-4640-9081-5efbc11122db" />
</p>


!IMPORTANT! When creating your Username and password for your VM, make sure to record or write down what your credentials are for later use. It is very easy to get confused when you have multiple VM's deployed. Keeping record of each one as well as its name and resource group can cut down on time searching or becoming lost in your own work.
This is used to connect through Remote Desktop Connection (RPD)
<p><img width="814" height="166" alt="image" src="https://github.com/user-attachments/assets/6cdafa5f-52a2-46af-b270-5c306e9e02b3" />
</p>


Finally click on Licensing. 
When you’re creating a Virtual Machine in Azure, the “Licensing” option at the bottom is about how the operating system (usually Windows) is licensed—and whether you can save money by using a license you already own.

If you CHECK it:
You’re telling Azure:
“I already own a valid Windows Server license”
Azure won’t charge you for the Windows OS license
You only pay for:
Compute (CPU/RAM)
Storage
Networking

This is called Azure Hybrid Benefit
<p><img width="772" height="201" alt="image" src="https://github.com/user-attachments/assets/2cfb8f60-e47c-4909-8801-7bc57a262824" />
</p>

Next we will click on the Network tab at the top to shift tabs into network settings.
<p><img width="697" height="56" alt="image" src="https://github.com/user-attachments/assets/7312617c-fe7a-487a-9343-b69975f55712" />

</p>

You will keep your Virtual network the exact same as what you named it to begin with in the "Basics" tab.
It should automatically be set.

-Basics tab-
<p><img width="788" height="129" alt="image" src="https://github.com/user-attachments/assets/f5152910-2aa3-49f3-a7e5-e46fb1358522" />
</p>

-Networking tab-
<p><img width="819" height="142" alt="image" src="https://github.com/user-attachments/assets/2fa8e88b-4403-4e1d-9cc7-b2fe7fb393ef" />
</p>

Those are the basics needed to set up a Virtual machine. The other tabs arent neccessary for this lessons.
At the bottom click Review + Create and give it a few minutes for your Virtual Machine to deploy!
<p><img width="479" height="41" alt="image" src="https://github.com/user-attachments/assets/25ea82e9-1019-432e-bdce-c86438b43299" />
</p>

This is just a basic page upon validation with the information and pricing regarding your VM just Click Create at the bottom.
<p><img width="817" height="825" alt="image" src="https://github.com/user-attachments/assets/fdac9c5e-eb6b-4acb-81fb-0dfb9dd10a7f" />
</p>

Once Complete navigate back to your resource group and find your Virtual machine.
<p><img width="1656" height="778" alt="image" src="https://github.com/user-attachments/assets/2f2f24dc-6b3d-4914-aaba-77dddf2ad9e4" />
</p>

To connect to your Virtual Machine through RDP (Remote Desktop Protocol) you will need your virtual machines PUBLIC IP.
Click directly on your Virtual machine and scroll through the properties.
You should find Public IP directly at the top.
<p><img width="1656" height="778" alt="image" src="https://github.com/user-attachments/assets/7f31fb3b-17bc-400f-926a-4f034ed9780e" />
</p>

<p><img width="1348" height="653" alt="image" src="https://github.com/user-attachments/assets/66b7211a-69f2-4631-866a-ed42236476d7" />
</p>

Some key notes for understanding your virtual machine and how to "Turn it on or off"
At the top of your Virtual Machines tab you will see "Start, Restart, and Stop" These are used to turn On or off your Virtual machine as well as restart it should you need to for any updates or current changes.
To check the status of your Virtual machines you will also see a "Status" tab stating the current status of your Virtual Machine.
As you can see I currently have 3 Virtual machines created. Two of which I am currently not using so I have stopped those and shut the service down to save money and our current server we just created is running.
<p><img width="1667" height="653" alt="image" src="https://github.com/user-attachments/assets/2ea75695-a4a4-4d0f-856e-9893ee02bcb4" />
</p>

Next we will navigate to our Remote Desktop Protocol.
In the start menu simply type Remote Desktop Connection and it will pop up.
Click it and you will see the RDP program open up.
<p><img width="386" height="929" alt="image" src="https://github.com/user-attachments/assets/671ee07c-5acd-403f-b558-b3feee62304a" />
</p>
<p><img width="404" height="241" alt="image" src="https://github.com/user-attachments/assets/bccfd42f-6a88-4a2d-8a8d-39627098834c" />
</p>

In your Remote Desktop Connection, Copy and Paste the PUBLIC IP from your Virtual Machine into the "Computer:" section.
It should look something like this. (IP will Differ)
<P><img width="402" height="239" alt="image" src="https://github.com/user-attachments/assets/90b7d458-561b-40d5-8592-ed21314c5641" />
</P>

Under that you will see "SHOW OPTIONS"
This is where you will take your Username you created earlier within the Virtual Machine set up and put that in this section and click Connect.
You will then be prompted for a password which will also be the password you had set in your virtual machine.
REMEMBER, As stated earlier this is a good example of why we keep record of our Usernames, Passwords and assosiating VM's so we do not get mixed up.
<br />
<p><img width="402" height="480" alt="image" src="https://github.com/user-attachments/assets/2b3de0d8-ce46-4327-bb2f-5c2c854e457e" />
</p>
<p><img width="459" height="457" alt="image" src="https://github.com/user-attachments/assets/f036c830-7368-40ef-96b3-1c507ee55f0f" />
</p>

Click Yes
<p><img width="408" height="480" alt="image" src="https://github.com/user-attachments/assets/1266a5a8-39ad-48e3-b9db-6bc9e1407004" />
</p>
Welcome to your Virtual Machine!
<p><img width="1918" height="1080" alt="image" src="https://github.com/user-attachments/assets/7ea37d02-473b-4d50-ab80-46e7b4735d1f" />
</p>

When finished you can simply close the connection by logging out, or by closing your remote desktop connection application.
<p><img width="449" height="211" alt="image" src="https://github.com/user-attachments/assets/5d214c01-ad35-4ab6-bdcf-76608e520866" />
</p>

!Important!
Make sure when you are done using your virtual machines that you TURN THEM OFF.
If kept running they will incur a cost. Whenever a Virtual machine is being used you pay for it the same way you'd pay an electrical bill.
Pay-per-use. So do not leave anything running unless nessecary.



-----
Remote Destop protocal / Connection (RDP) is a great system used by every technician and IT department to fix issues without being physically present. It is also a great way to work remotly while still having access to your own files, programs, and systems on a seperate machine. 
More indepth ways of using RDP and Virtual machines combined are with Domain Controllers and Active directory. 
Virtual machines are commonly used to manage domain controllers for ease of access. Administrators are able to remotely connect from anywhere to make permission changes, fix user account, errors, or changes as well as creating snapshot backups incase something goes wrong for quick and easy restoration.

Virtual Machines are a great way to reduce costs and resources by replacing the need for multiple physical computers. They help with ease of backups, cloning and system recovery
Azure creates a great space to navigate any of your cloud computing needs and I urge you to check out more of the possibilities within Azure
