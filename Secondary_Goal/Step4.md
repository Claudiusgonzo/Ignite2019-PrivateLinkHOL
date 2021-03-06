# Use the spoke VM to test connectivity to Azure SQL over Private link

1.	Return once more to your RDP session for VM-WIN-SPOKE.

2.	Open a the cmd app from the desktop and use nslookup to test your private DNS:
- nslookup labsqlXXXXXX.database.windows.net
- Hint: You can find your unique hostname by on the lab portal under Environment Details: Storage Account Name, or just peek at the SMSS login window if it’s still open. 
 
![alt text](https://github.com/microsoft/Ignite2019-PrivateLinkHOL/blob/master/images/2.4_2.png)

3.	Close the SSMS application and log back in, using the same values the __Connect to Server__ window as before (should be cached) 
- __Server name: labsqlXXXXXX.database.windows.net__
- __Authentication: SQL Server Authentication__
- __Login: demouser__
- __Password: demoPassword1!__

4.	In the Object Explorer window, navigate to Databases > labsqldb > __Tables__, then right click and make a new table and add in a few columns:

![alt text](https://github.com/microsoft/Ignite2019-PrivateLinkHOL/blob/master/images/2.4_4.png)

5.	Then go to __file > save__, name it “Table_2”, and click __okay__. 

6.	Congratulations, you are now securely managing your Azure SQL instance from VNET_SPOKE to a Private Endpoint in VNET_HUB, using nothing but RFC1918 private IP space. 


### Your POC has been a success, it’s time to ask your boss for a raise!
