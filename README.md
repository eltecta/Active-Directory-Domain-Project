Hi! Thanks so much for checking out my Active Directory project, let me know if you have any questions!

# Abstract
The main goal of this project was to set up an Active Directory homelab to gain familiarity with the software and practice my practical Windows server skills. In this project I detail my homelab and what I've done so far. The main feature of this homelab is a Domain Controller that runs Active Directory and uses RAS routing to allow client computers to gain network access by joining the domain. 
# Network Diagram
![Network Diagram](https://github.com/user-attachments/assets/e7ae33f3-0aa1-4485-9b44-7a342b6a27b9)
# Virtualbox Configuration
The entire homelab is set up in Virtualbox using an ISO of Windows Server 2019 for the Domain Controller and a Windows 10 Pro ISO for the Client
![vb1](https://github.com/user-attachments/assets/f1276f27-434e-403e-b1ca-9991e3089de7)
# Domain Controller Configuration
The Domain Controller is responsible for hosting Active Direcotry Domain Services as well as funcitoning as the DHCP server for any client computers connecting to the domain. It does this throught he use of two network adapters, one being an external network adapter that uses a bridged connection to my home network and a second network adapter for internal network interfacing, allowing client computers to use the internet through the DC. 
![Dc networking](https://github.com/user-attachments/assets/f3ac5e05-54a4-4ba4-88be-1e5b7d9dd593)
The DC's DHCP configuration assigns IP addresses in the range of 172.16.0.100 to 172.16.0.200
![dhcp](https://github.com/user-attachments/assets/36e12aa8-ef15-4b6d-a6c8-b16764311aa3)
## Active Directory Configuration
My first order of business was creating a user with administrative privileges to allow myself to configure the rest, creating a copy of the default administrator profile and giving it my login credentials. 

![ad123](https://github.com/user-attachments/assets/90b57119-c84d-4dfe-9acb-5090703f5169)

![asdda](https://github.com/user-attachments/assets/c7360f6e-e14a-45d3-8431-6ec26f7aac21)

After this I created a few sample Organizational Units to familiarize myself with the process as well as setting up some example users so that I could test joining the domain and logging in as a user, these users were created with standard privilege
![ad3](https://github.com/user-attachments/assets/bcb459b0-fb1b-4761-8418-08caacba19a8)
# Client Configuration
The client uses a single network adapter that only connects to the local network, through that, I joined my Active Directory Domain, logged in as one of the sample users I created and I was able to access the internet!
![ddd](https://github.com/user-attachments/assets/1371709f-7d6f-47b8-b562-6d138fc949f1)
![aadad](https://github.com/user-attachments/assets/74c0de18-40da-42f6-9c48-6e9db0a16bc5)
![ad12](https://github.com/user-attachments/assets/31d61f98-cdb7-407e-ad09-781354df7e5c)
After this I switched back over to my DC VM and checked to see if the connection registered
![ad2](https://github.com/user-attachments/assets/1edf5670-198c-4f16-ae52-2fd800bcd127)
Very relieved to see that the connection was being recognized in the Active Directory Users and Computers applet

# Conclusion
Thank you so much for taking a look at my Active Directory project, it was really fun ot interact with this software I had heard so much about during my studies and I was super relieved to find how intuitive the whole process was. 
