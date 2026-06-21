Initial Windows Server Setup and Installing Active Directory Domain Services

Description

This project documents my initial Windows Server installation and the steps I took to install and configure Active Directory Domain Services (AD DS), including promoting the server to a domain controller.

Languages and Tools Utilzied 

Active Directory
CMD


Enviroements
VMWare
Windows Servwe 2025


Links



Program walk-through
diamgram showing what ill be doing in this first project 



Starting off I will begin renaming the server 
 Rename the server to something clear as the default name is very random and most times meaningless like (WIN-K3J9XYZ), while a name like FileSever01 instantly tells you its function in the process. You also want to do this before promoting it, since renaming a domain controller afterwards is a headache.

<img width="318" height="185" alt="image" src="https://github.com/user-attachments/assets/cd6730ea-109b-4152-9ab7-d314a90d34db" />
(you must restart VM for rename to apply)

to make sure its taken affect pull up command prompt (type in cmd in search below) then type in hostname it should return FileSever01)

<img width="447" height="150" alt="image" src="https://github.com/user-attachments/assets/e7799a60-21f2-4a6f-804d-828a6472aeac" />

Before doing anythign else it is important to Configure Windows Updates to the server  full pacthed, stable,and secure. and because updates require multiple reboots you dont want it to intertupt when you are configurting ur domain 

CLick on settings go to windows update and make sure server is up to date 
<img width="703" height="165" alt="image" src="https://github.com/user-attachments/assets/ba423400-eda3-4f59-ac6e-8b5a15b8b12f" />

Next we will be enabling remote managment 
This is really important for servers so you can manage the servers without logging into it directly. You can log into it using any computer in the network and this also mimics real-world practice.  
  
To enable remote management just search for the Server Manager and open it. On the left side you will see Local Server and click on it. Usually it's enabled but just make sure it's enabled. If not, click on it and you can check to enable remote management for the server.

<img width="226" height="16" alt="image" src="https://github.com/user-attachments/assets/dabfa4c7-9f5a-4582-b1f5-09ca618927d5" />

Next we we will be installing active direcorty domain services 
First open up server manager  on the top right click on add roles and features click next intll u get to server roles make sure to check active doirectory domain services 
<img width="780" height="548" alt="image" src="https://github.com/user-attachments/assets/10752681-5524-4783-8b33-c800f82f8713" />
click next untill you see install it is also very important not to close the wizrd once it has finsih the isntalltaion beacuse our next step will be promotign a this sever to a domain controller in the nedt step

After instalation is complete click on promote this sever to a domain controller 

<img width="781" height="547" alt="image" src="https://github.com/user-attachments/assets/5e771429-6a35-4861-920a-44fdb47775a0" />

a new window will open and click on add a new forest in the boix below we will be making a domain domain name since this is a homelab avoid using a real domain names so just use something like homelab.local
it is also important to check your spelling as a small typo such as .lcoal in your domain name can become a hassle to fix.
<img width="757" height="547" alt="image" src="https://github.com/user-attachments/assets/285273d9-e4eb-4fd8-9710-81ea8749ff9d" />

make sure that windows server 2025 is selected 
<img width="756" height="545" alt="image" src="https://github.com/user-attachments/assets/eb590cff-a61f-47ee-94aa-4c75aa25b798" />

next chooser a password and keep it somewhere safe as trying to remembers isnt allways gurrranted.

then click on next until review options and take a sec to review evyerthing snd make sure thast the domain name is correct 

Next you should see all prereqquietes checks passed however if you see an error jsut click on prebious and click agasin on the nexct sometimes it takes a sec for preqreqs to pass

<img width="727" height="33" alt="image" src="https://github.com/user-attachments/assets/82d7731f-fddf-478e-8504-f37e02be9561" />

You will then see a sign out box just click close 

<img width="598" height="194" alt="image" src="https://github.com/user-attachments/assets/3432073e-2504-4f7f-a260-af1ebcddf15a" />

after rebooting you should see that your server is now a domain controller and domain name should be seen










 
