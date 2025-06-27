 1. Opened Windows Firewall:
- Used "Windows Defender Firewall with Advanced Security" from the Start menu.

 2. Blocked Port 23 (Telnet):
- Created a new inbound rule in Windows Firewall:
  - Protocol: TCP
  - Port: 23
  - Action: Block the connection
  - Applied to: Domain, Private, Public
  - Rule name: `Block_Telnet`

3. Enabled Telnet Client:
- Went to "Turn Windows features on or off" and enabled **Telnet Client**.

 4. Tested the Rule:
- Opened Command Prompt and typed:telnet localhost 23

- Result:  
Could not open connection to the host, on port 23: Connect failed
✅ This confirmed that the firewall rule was successfully blocking the port.

5. Deleted the Rule:
- After testing, deleted the `Block_Telnet` rule to restore original firewall settings.

