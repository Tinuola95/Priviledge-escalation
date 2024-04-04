# Enumeration and Priviledge escalation Lab

<p>
  <h3>Description</h3>
In this laboratory session, we will utilize tools available in Kali Linux, such as nmap, to perform a comprehensive enumeration of a designated target system. Through this process, we aim to identify vulnerabilities within the target system's infrastructure and subsequently exploit these vulnerabilities to establish a foothold. Furthermore, we will explore techniques to escalate our privileges within the target system, ultimately seeking to attain root access.

<p>

<h2>Tools </h2>

- <b>nmap</b>
- <b>PwnKit</b> 

<h2>Environments Used </h2>

- <b>Kali Linux 6.5.0 </b>
- <b>Windows 11</b>

<h2>Lab walk-through:</h2>

<p align="center">
Installing Splunk Enterprise on Windows 11 Host: Check the box to accept License Agreement and Click Next<br/>
<img src="https://imgur.com/lhxJcE0.png" height="80%" width="80%"/>
<br />
<br />
Create an Admin Account and Click Next<br/>
<img src="https://imgur.com/wCXTRQC.png" height="80%" width="80%" />
<br />
<br />
Click install<br/>
<img src="https://imgur.com/w280tvX.png" height="80%" width="80%" />
<br />
<br />
Setup Installing<br/>
<img src="https://imgur.com/wu3MgE5.png" height="80%" width="80%" />
<br />
<br />
Installation Complete: Click finish<br/>
<img src="https://imgur.com/NO49ZCC.png" height="80%" width="80%" />
<br />
<br />
Splunk Enterprise is launch with the default home page <br/>
<img src="https://imgur.com/EflRwzk.png" height="80%" width="80%" />
<br />
<br />
Navigating Splunk: Splunk bar includes: Messages(For system level messages),Settings(For configuration),Activity(To review job progress),Help and
Find(For Search)<br/>
<img src="https://imgur.com/h7u1VT1.png" height="80%" width="80%" />
<br />
<br />
App Panel: Allows for ability to see installed apps on splunk instance with one of its default App:Search and Reporting<br/>
<img src="https://imgur.com/IKo5OkY.png" height="80%" width="80%" />
<br />
<br />
Explore Splunk: Gives quick links to add data,add new apps and access splunk documentation.<br/>
<img src="https://imgur.com/1e10xFB.png" height="80%" width="80%" />
<br />
<br />
Splunk Dashboard: No Dashboard are display by default: You an create Dashboard<br/>
<img src="https://imgur.com/6DNwyhi.png" height="80%" width="80%" />
<br />
<br />
Splunk Dashboard Continues: You can choose from a range of dashboard from the dropdown menu or by visiting the Dashboard listing page<br/>
<img src="https://imgur.com/vrodWdX.png" height="80%" width="80%" />
<br />
<br />
Adding or Ingesting Data into Splunk Instance: Click on Add data on the Explore Splunk home page and a new page like this appears<br/>
<img src="https://imgur.com/XPF50bQ.png" height="80%" width="80%" />
<br />
<br />
There are few ways we send data to splunk such as Monitor, forwarder but we will use the upload option: A page like this will appear <br/>
<img src="https://imgur.com/jJb4mk4.png" height="80%" width="80%" />
<br />
<br />
This page allows you to select the Log Source(VPNlogs) stored on our computer:Select the file from your Computer, upload and Click Next<br/>
<img src="https://imgur.com/jJb4mk4.png" height="80%" width="80%" />
<br />
<br />
Select Source Type :This page shows how splunk sees my log source type.:Splunk identified it as json. Click Next<br/>
<img src="https://imgur.com/0FMAyuK.png" height="80%" width="80%" />
<br />
<br />
Create an Index where the logs will be dumped:Index takes the data uploaded and normalizes it into value pairs, data type and store as events.Click save<br/>
<img src="https://imgur.com/T51Oaea.png" height="80%" width="80%" />
<br />
<br />
Create a host field value with a name from which the events originated from.In this event is from VPN connection: Select the index created in the dropdown and Click review <br/>
<img src="https://imgur.com/tLFU5RS.png" height="80%" width="80%" />
<br />
<br />
Review Page shows the Input Type, File Name, Source Type and the created Host and Index.Click Submit and then Click Start Searching<br/>
<img src="https://imgur.com/EVkwzdm.png" height="80%" width="80%" />
<br />
<br />
Page Appears showing all the logs been ingested and  indexed(with field-values and data types) into Splunk Instance <br/>
<img src="https://imgur.com/nlhqrf9.png" height="80%" width="80%" />
<br />
<br />
 Below shows number of events indexed and ingested into the splunk instnace: 5724 Events<br/>
<img src="https://imgur.com/LXqZ2eW.png" height="80%" width="80%" />
<br />
<br />
I index search on the Username Maleena to identify how many Log Events was captured: 120 Events <br/>
<img src="https://imgur.com/khrQpZH.png" height="80%" width="80%" />
<br />
<br />
I index search the Username associated with the IP Address 107.14.182.38: Smith has the IP <br/>
<img src="https://imgur.com/JasJVty.png" height="80%" width="80%" />
<br />
<br />
I index search the number of events originated from all countries except France: I index search France event and subtract it from total event. <br/>
<img src="https://imgur.com/0W69cOX.png" height="80%" width="80%" />
<br />
<br />

<h2>Conclusion</h2>
Again, this is just a basic overview of Splunk where I just uploaded a network centric data(VPN LOGS) into Splunk Instance and did a simple index searches.We can also have a Splunk forwader which is one of the component of Splunk install and configured on Host machine to capture host centric logs example(winEvent logs) and forwards it to the Splunk instance for investigation or Analysis(This is going to be my next project). We can also create table for specific Indexes or field value types to reduce search.




</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
