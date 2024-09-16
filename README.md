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
<br />
  
Setup Vultr: I start by heading to the Vultr cloud provider website and setting up my cloud account. https://www.Vultr.com<br/>
<img src="https://i.imgur.com/Iw0Tngo.png" height="80%" width="80%" alt="Setup"/>
<br />
<br />

<br />
  
After setting up my account, I head over to products and create my VPC.<br/>
<img src="https://i.imgur.com/izhEEse.png" height="80%" width="80%" alt="Setup"/>
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


</p>
