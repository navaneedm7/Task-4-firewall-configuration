#####                              **Firewall Configuration and Testing Report**







###### **1.Objective**



To configure and test basic firewall rules in Windows Defender Firewall to block and allow specific network traffic and understand how firewall filtering works.







###### **2.Tools Used**



* Operating System: Windows 11
* Firewall Tool:



&nbsp;    Windows Defender Firewall



* Testing Tools:

&nbsp; 

&nbsp;    telnet







###### **3.Viewing Current Firewall Rules**



Steps:



1. Press Win + R
2. Type wf.msc
3. Press Enter
4. Click on Inbound Rules



This displays all currently configured inbound firewall rules.







###### **4.Creating a Rule to Block Port 23 (Telnet)**



Steps Performed:



1.Open Windows Defender Firewall

2.Click Inbound Rules

3.Click New Rule

4.Select Port

5.Choose TCP

6.Enter specific local port: 23

7.Select Block the connection

8.Apply rule to:

* Domain
* Private
* Public

9.Name the rule:

&nbsp;Block Telnet Port 23

10.Click Finish



The rule is now active and blocking inbound traffic on port 23.







###### **5.Testing the Firewall Rule**



&nbsp;  Command Used:



&nbsp; telnet localhost 23



&nbsp;  Output:



&nbsp;    Could not open connection to the host, on port 23: Connect failed







###### **6.Removing the Test Rule**



After testing:



1. Open wf.msc
2. Go to Inbound Rules
3. Locate Block Telnet Port 23
4. Right-click → Select Delete



This restores the system to its original state.







###### **7.How Windows Firewall Filters Traffic**



Windows Defender Firewall filters network traffic based on:



* Port number (e.g., 23 for Telnet)
* Protocol (TCP or UDP)
* Direction (Inbound or Outbound)
* Rule action (Allow or Block)
* Network profile (Domain, Private, Public)



When traffic matches a rule condition, the firewall either allows or blocks the packet according to the configured action.







###### **8.Conclusion**



In this task, a firewall rule was successfully created to block inbound Telnet traffic on port 23. The rule was tested using PowerShell, and the connection attempt failed as expected. After verification, the test rule was removed.



This task demonstrates practical firewall configuration skills and an understanding of how Windows Firewall controls network traffic.



