## Checking Current Firewall Status (Windows)
To verify whether the firewall was active before making any changes, the firewall status was checked using Command Prompt.
### Command Used
netsh advfirewall show allprofiles
### Explanation
- `netsh` → Command-line tool used to configure network settings.
- `advfirewall` → Refers to Windows Advanced Firewall settings.
- `show allprofiles` → Displays the status of all firewall profiles (Domain, Private, Public).
### Output Observed
The output displayed the following:
- Domain Profile State: ON
- Private Profile State: ON
- Public Profile State: ON
### Analysis
The "ON" status confirms that the firewall is enabled for all network profiles.  
This means the system is actively filtering inbound and outbound traffic based on configured firewall rules.

Checking the firewall status before configuring new rules is important to:
- Ensure firewall protection is active
- Understand current security posture
- Avoid modifying a disabled firewall configuration
