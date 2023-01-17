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
