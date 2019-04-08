# How the Internet Works and Linux
# How the Internet Works - AFS Tutorial by David Salazar
# April 7th, 2019


### Logging Into AFS 

1.Go to tools, Start SSH session, edit credentials.

![alt text](img/AFSlogging1.PNG)

2. In the following window,

![alt text](img/AFSLogging2.PNG)

    Enter the following, 
    * Host: afs(any number between 1-22).njit.edu
    * Port: 22
    * User name: your ucid username
    * Password: your ucid password
    
3. The following terminal window shows after successfully logging into AFS, 

![alt text](img/AFSLogging3.PNG)


### Deployment
used to have files of a website locally and linked to a website remote 

1. Go to tools, Deployment, and select configuration, click on the + tab, name host, select SFTP

![alt text](img/AFSLogging4.PNG) 

    Enter the following, 
    * Host: afs(any number between 1-22).njit.edu
    * Port: 22
    * User name: your ucid username
    * Password: your ucid password
    * Test Connection. Make sure that the root path has /ucid/public html
    * Webserver URL should read: http://web.njit.edu/~dfs23
    
2. In the deployment window select Mappings and add / in the Deployment path 

![alt text](img/AFSLogging5.PNG)

3. Add a .gitignore file to your project, and include .idea inside the file, and commit
![alt text](img/AFSLogging6.PNG)

4. Select Tools, Deployment, Automatic upload

5. Tools, Deployment, Browse Remote Host. The remote host w/ files will appear on the upper right side of your screen.
![alt text](img/AFSLogging7.PNG)

6. Scroll over to the location of your remote host afs files (in step 5), and right click on the index.html file. 
   Select the download from here option. Commit now. 

7. Select VCS, import into Version Control, select share project on Github, press ok. 
   



### Terms to Know 
1. Secure Socket Shell (SSH): used for sending text files 
2. Port 22 in SSH: utilizes encryption
3. Standard File Transfer Protocol (SFTP) :      known as Secure Socket Shell, and this 
                                                 sets up files that get automatically updated
                                                 in the afs server. the S in front of FTP means 
                                                 that encryption is used. In order for encryption
                                                 to be used, Port 22 was selected
4. File Transfer Protocol (FTP) :       does not use encryption. and as a result Port 21 is used when 
                                        selecting a host 

5. HTTP: hyper text transfer protocol 
6. HTTPS: secured hyper text transfer protocol 
7. ICAN: runs Domain Name Server (DNS). ICAN uses trees to run DNS servers
8. Hierarchy of servers: there is a layer of DNS servers before the ICAN server can be reached 
9. Software Protocol: an agreement on something being done. 
10. Browser and functions: 
    
    
    * browsers are used to connect to the web browser
    * Browser sends the requests, 
        1. get    : request to get a webpage
        2. post   : post new records
        3. put    : make updates
        4. delete : delete 
        5. patch  : update selectively 

11. URL : Universal resource locator (unique address). 

Roy Fielding's Dissertation

Describes how the internet can be used as agiant database with Representational State Transfer(REST). The reason for 
using the internet as a giant database is to make it easier to share information around the world. REST was used as a 
guide to design and develop the architecture of the modern Web[1]. REST was used in the design of Hypertext Transfer 
Protocol and Uniform Resource Indentifier standards from their deployment in Web client and server software.

source:     1. https://www.ics.uci.edu/~fielding/pubs/dissertation/fielding_dissertation.pdf

Important Terms:

DNS- The Domain Name System is a hierarchical and decentralized naming system for computers, services, or other resources connected to the Internet or a private network.
     name -> ip: forward look up. ip -> name: reverse look up
IP-  is the principal communications protocol in the Internet protocol suite for relaying datagrams across network boundaries.

Top Level Domain(TLD)- one of the domains at the highest level in the hierarchical Domain Name System of the Internet. It has a direct connection to ICAN

