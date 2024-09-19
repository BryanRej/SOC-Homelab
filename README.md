<h1>SOC Homelab</h1>

<h2>Description</h2>
This project uses the VULTR cloud provider and various virtual machines to simulate a Security Operation Center environment implemented through eight virtual machines.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Linux, Powershell, Splunk </b> 


<h2>Environments Used </h2>

- <b>Vultr Cloud, Ubuntu Server, Windows Server, Windows 10, Kali Linux, Fleet Server, Mythic server, osTicket. </b> 

<h2>Project walk-through:</h2>

<p align="center">
  Create a Logical Diagram: I used draw.io to create a digital logical diagram of the entire network, its connections, and workflows. The IP ranges will be automatically configured through VULTR.  <br/>
<img src="https://i.imgur.com/T9p1jPl.png" height="50%" width="50%" alt="Diagram creation"/>
<br />
  
Setup Vultr: I start by heading to the Vultr cloud provider website and setting up my cloud account. https://www.Vultr.com<br/>
<img src="https://i.imgur.com/FaqRuDa.png" width="80%" alt="Setup"/>
<br />
<br />

<br />
  
After setting up my account, I head over to products and create my VPC.<br/>
<img src="https://i.imgur.com/7RbVead.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/RB7Jw1J.png" height="80%" width="80%" alt="Setup"/>
<br />

I decided to remote into the server instead of using the server's console. I then updated the server and began installing/configuring ElasticSearch and Kibana. <br/>
<img src="https://i.imgur.com/7oaeTmI.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/dnts08L.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/fgY4hmx.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/V9Y13HW.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/pHbEhRE.png" height="80%" width="80%" alt="Setup"/>
<br />

Next, I adjusted the firewall rules of the ELK server within VULTR. <br/>
<img src="https://i.imgur.com/nuuhrKs.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/avc9XC4.png" height="80%" width="80%" alt="Setup"/>
<br />

Now, I begin setting up my Elastic instance. <br/>
<img src="https://i.imgur.com/g3qakMC.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/DfpIUFG.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/gViZh6T.png" height="80%" width="80%" alt="Setup"/>
<br />

Logging into the instance. Configuring Kibana key stores and API encryption tokens. <br/>
<img src="https://i.imgur.com/YIW6s2M.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/HyyM19J.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/V985f4g.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/ofSPAue.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/ELjzRMN.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/2Csc60F.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/rEQ80HW.png" height="80%" width="80%" alt="Setup"/>
<br />

Creating my Windows Server with RDP enabled. It will be separated from my VNC for safety reasons.  <br/>
<img src="https://i.imgur.com/TG5zq5R.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/XLfUILW.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/j6jRdRN.png" height="80%" width="80%" alt="Setup"/>
<br />

Creating and updating my Ubuntu fleet server. <br/>
<img src="https://i.imgur.com/nuuhrKs.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/kbkAhz1.png" height="80%" width="80%" alt="Setup"/>
<br />

Adding my fleet server and Elastic agent from the Windows server to the Elastic web Gui instance. <br/>
<img src="https://i.imgur.com/TwNXHQN.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/TQ97ATO.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/w1sF3YD.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/U8ohE9L.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/wfej6j1.png" height="80%" width="80%" alt="Setup"/>
<br />

<br />

Installing Sysmon along with a special configuration file on my Windows server for endpoint detection. <br/>
<img src="https://i.imgur.com/QhiOrjV.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/Axl4APa.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/NrMqCAe.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/CEU6nl7.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/HHpodL5.png" height="80%" width="80%" alt="Setup"/>
<br />
Integrating my Windows server Sysmon and Windows Defender logs into my Elastic instance. I needed to adjust the firewall rules on my VPC to allow incoming traffic from the correct port to enable viewing of the Windows server telemetry. <br/>
<img src="https://i.imgur.com/uLgHz7m.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/Y8DlClS.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/V1DETRb.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/MQou6VC.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/tCsP6OX.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/bSh7lIx.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/Hlq6JuY.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/uwNRSRs.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/ZlSetzK.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/iWgZrfg.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/KF7G5Jj.png" height="80%" width="80%" alt="Setup"/>
<br />

Creating and updating repositories  for my Ubuntu SSH server. Checking auth.logs file for any data on authentication attempts. <br/>
<img src="https://i.imgur.com/lUxDcyR.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/2vp8S9t.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/0kvpdiZ.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/DedqfcO.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/sSYc5YA.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/weyVtte.png" height="80%" width="80%" alt="Setup"/>
<br />

Installing Elastic agent onto the new Ubuntu server and integrating the logs to my Elastic instance. Modifying the network firewall to allow traffic from the Ubuntu server. Examining suspicious authentication attempts for my root user from specific IP addresses in Elastic. <br/>
<img src="https://i.imgur.com/kYq3p3v.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/5gJgFqT.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/sdN3hZx.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/8NnPjCJ.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/CPwc7b7.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/BMZuQHk.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/7nmHxCB.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/aVuFVX9.png" height="80%" width="80%" alt="Setup"/>
<img src="https://i.imgur.com/iNZ1yTH.png" height="80%" width="80%" alt="Setup"/>
<br />

</p>
