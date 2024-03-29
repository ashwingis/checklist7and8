**WEEK 07 and 08 Technical Logbook**

**Name**: Ashwin Balaji Srinivasan 

**Course**: GEOM99 Web GIS Development 

**Time-Taken**: 3 Hours 

  

**Description** 

**Create and use a Technical Activity Log**

Created a Technical Log in Excel and made pages for each week. Created a word file for log descriptions. 

**Create a virtual machine**

1. Access https://console.cloud.google.com/compute  

2.Create a new GCP billing project  

3.Assign the academic credits to this project  

4.Select the project to make sure to stay in the same project throughout.  

5.enable CGP Compute Engine API   

6.Create the new virtual machine Instance  

7.Name the Virtual Machine 'arcgisserver-geom99'  

8.Change the Boot Disk to use instructor's image 'geom99-2023-v2' by selecting 'Shawn's ArcGIS Server'  

9.Allow HTTP and HTTPS traffic by checking under the 'Firewall'.  

10.Finally create the virtual machine. 

**Set Password**

1. Once the VM get a green tick in the status, Click the drop-down arrow near RDP under connect and click set password.  

2.Give the username as 'student' and click set.  

3. A new password is generated.  

4. Save the password in notepad. (Won't get to see the password again!) 


**Set Firewall Rules**

1.Under Cloud NGFW, click Firewall policies and click 'Create Firewall Rules'.  

2. Set the name to be flemingrdp444 and targets as 'All instances in the network'. 

3. Under Source filter, select IPv4 ranges and set source IPv4 ranges to '0.0.0.0/0' so there are no restrictions to access. (It can be modified at any point)   

4.Set the TCP port to 444 (on-campus students) and create the New Firewall Rule.  

5. Repeat the same process to create another rule but give the name as 'arcgisserveradmin'. Repeat the same for targets and source filter.  

6. Mention the ports 6443, 6080 in the TCP ports and create the new rule. 

**Access the Remote Desktop**

1. From start, access the Remote Desktop Connection tool and enter the external IP address from VM 'arcgisserver-geom99' with a colon and the port 444.  

2. Once connected, it asks for the credentials and click use a different account and enter 'student' as username and the 'password saved in the notepad' as password.  

3. Click yes to the window that shows 'certificate is not from a trusted certifying authority'. 

**Allow ArcGIS Server Management Ports in the remote desktop **

1. After entering the remote desktop, in the start menu, search for Windows Defender Firewall with advance security.  

2. Click the inbound rule from the left pane and select 'New Rule' from the right pane. 3. Select 'Port' and 'TCP' and 'Specific local ports'.  

4. Under 'Specific local ports' type 6443 and 6080 and finally I named the rule as 'arcgisserveradmin'.  

5. Check 'Allow the connection' and click 'Finish'.   

**Extracting data on my remote desktop and importing data in ArcGIS Pro (local computer)**

1.In the remote desktop, unzip the Canada.zip file and paste the content in 'c:\gisworkspace\Canada'.  

2.In my desktop, create a folder 'gisworksapce' in C directory and a sub folder 'Canada' within it.  

3.Open ArcGIS Pro and create a new file and copy the Canada shapefile from the same file directory.  

4.Change the symbology as preferred. 


**Publishing data to my server**

1. In ArcGIS Pro, go to 'Insert' and click 'Connections' and select 'New ArcGIS Server' within 'Server'.  

2. Type the external IP address with '6443'port with /arcgis.  

3. Enter the user ID and password as given in the D2L and give 'OK' to create a new ArcGIS Server.  

4. To make the publishing organised, I created a folder in my server manager.  

5. Now I am publishing the data to my server, and I clicked analyse and assigned a unique ID and registering the data folder to my server.  

6. Once the map is published, I went to the REST end point and copied the URL and published it on ArcGIS Online as a feature layer.  

7.**Reference**: https://130.211.126.157/arcgis/rest/services/Ashwin_Mappublishing/Canadaassriniv/MapServer/0
    

 

 
