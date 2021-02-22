# Appspace-Ver-6.2.4-Stored-Xss
Stored cross Site scripting Vulnerability in appspace Web Framework version 6.2.4 

Observation: Stored cross site scripting vulnerability was observed in the appspace platform version 6.2.4. After a user gets authenticated and and enters an xss payload under groups section of the network tab it gets stored as the group name.Whenever another player or member visits that group this payload gets executed.

Steps To reproduce:

1. Login to appspace
2. Go to the admin tab from the drop down on the left and select Users.
3. Create a group under any network with xss payload(use the same payload as given in the POC) in the Name field and save.
4. Xss payload will pop up on the screen 

Impact : Users can be invited to join a network's group with xss payload in the name of the group and once a new user Opens this group xss will pop up and thus attacker could steal session cookies, redirect user to phishing site , steal data using JS keylogger etc.

POC: Image POC's have been given below:

