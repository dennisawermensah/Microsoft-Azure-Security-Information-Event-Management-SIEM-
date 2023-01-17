<h1>Microsoft Azure Security Information Event Management (SIEM)</h1>


<h2>Description</h2>
This project walks the user through enhacing Microsoft Azure Microsoft Azure Security Information Event Management (SIEM)<br>
<br />

<h2>Walk-through:</h2>
Sign up for a free Azure subscription<br>
<p align="center">
<img src="https://i.imgur.com/Xc7rXUs.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
<br />

<h3>1. Creating a Virtual Machine.</h3> <br>
I. Search for Virtual Machine in the search box and press enter.<br>
II. Create a Virtual Machine by filling out all required fields under 'Basics'
<p align="center">
<img src="https://i.imgur.com/89alnnl.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
<br />
<p align="center">
<img src="https://i.imgur.com/w2w1qap.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
<br />
  
III. Under Networking, click on the radio button for 'Advanced'., click on 'Create new'<br>
<p align="center">
<img src="https://i.imgur.com/TJ2SuZk.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
<br />

IV. 'Add an inboud rule' that allows for any connection (goal is to make the network vulnerable), click 'Review + create'<br>
<p align="center">
<img src="https://i.imgur.com/hg6PIdR.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
<br />
 
V. Create a log analystics workspace<br>
<p align="center">
<img src="https://i.imgur.com/Psq5VQo.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
<br />

VI. Go to Microsoft Defender for Cloud , Click on 'Environment settings', Click on the Log Analystics Workspace created earlier under your subscription <br>
<p align="center">
<img src="https://i.imgur.com/avhrd3o.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
<br />

VII. In 'Defender plans' turn 'On' Servers and save<br>
<p align="center">
<img src="https://i.imgur.com/TJ7N20p.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />

VIII. In 'Data Collection' click on the radio button for 'All Events' and save.<br>
<p align="center">
<img src="https://i.imgur.com/VBkB5lz.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
<br />

IX. Go to the Log Analytics Workspace created, click on Virtual machine, click on the virtual machine created. Click on 'Connect'<br>
<p align="center">
<img src="https://i.imgur.com/xoVSt7v.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
<p align="center">
<img src="https://i.imgur.com/3Vnexr7.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />

X. Go to Microsoft Sentinel, Click on 'Create', select the log analystics workspace created, click 'Add'<br>
<p align="center">
<img src="https://i.imgur.com/W1xax4I.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
<p align="center">
<img src="https://i.imgur.com/8GUueKI.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />

XI. Go to the VM created, copy the public IP and connect to Remote Desktop<br>
<p align="center">
<img src="https://i.imgur.com/RHFHjPo.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
<p align="center">
<img src="https://i.imgur.com/aP4G2Yj.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
  
X. In the remote desktop, go to Event Viewer, click on Windows Log, then Security. We see login audits <br>
<p align="center">
<img src="https://i.imgur.com/8Nhf4jB.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
  
XI. Ping the Public IP of Remote desktop on your local pc <br>
<p align="center">
<img src="https://i.imgur.com/j7VR07R.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
  
XII. Turn off firewall in Remote Desktop. Check the ping message on local pc <br>
<p align="center">
<img src="https://i.imgur.com/sKableZ.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
  
XIII. Open PowwerShell and paste custom script and run in the remote desktop to gather logs for  logins <br>
<p align="center">
<img src="https://i.imgur.com/2rQPYDB.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
  
XIV. In Azure portal, go to Log analytucs workspace created, click on custom logs, click on 'Add custom logs' <br>
<p align="center">
<img src="https://i.imgur.com/xY31yET.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
  
XV. Locate the failed_rdp.log file which has all log data, copy and paste onto notepad on local pc and save. <br>
<p align="center">
<img src="https://i.imgur.com/CmcLnQx.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
  
XVI. Click on the folder icon to load the saved logs in the notepad on the local pc <br>
<p align="center">
<img src="https://i.imgur.com/PZlLGjO.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
  
XVII. Copy 'failed_rdp.log' location from remote desktop to 'Collection paths' in 'custom log' <br>
<p align="center">
<img src="https://i.imgur.com/tjKmxFG.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
  
XVIII. give a custom name <br>
<p align="center">
<img src="https://i.imgur.com/TG2m3l4.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
  
XIX. click on logs and run the custom name to see the logs collected <br>
<p align="center">
<img src="https://i.imgur.com/tnxeT1l.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
  
XX. Extract fields and give them labels <br>
<p align="center">
<img src="https://i.imgur.com/w77LUl9.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
  
XXI. Go to Microsoft Sentinel and 'Add Workbook' <br>
<p align="center">
<img src="https://i.imgur.com/e8emCH0.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
  
XXII. Remove all templates and 'Add query' <br>
<p align="center">
<img src="https://i.imgur.com/lzAtkls.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
  
XXIII. Run custom query, Visualize by map <br>
<p align="center">
<img src="https://i.imgur.com/NXAOkWV.png" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
 
XIX. Refesh Map for new uploaods
<p align="center">
<img src="" height="80%" width="80%" alt="Deploy Virual Machine"/>
<br />
  
XXX. Apply frameworks to remediate/mitigate risks.
  
