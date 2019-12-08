# MVP Advent Calendar
Welcome to the gift I have prepared for you for the 9th day of the MVP Advent Calendar. 
Thanks to Megan Walker for the great idea of bringing all the MVPs together for a great advent calendar. 

I hope you enjoy it!

## Create an Azure AD App with Graph API permissions
To use these Flows successfully you should create an Azure AD App. My colleague Gustavo Velez wrote a very good blog about how to create this. He uses the `SecurityEvents.Read.All` permissions, which we are not gonna use. Use the `User.Invite.All` permissions for Flow 1 and the `Group.ReadWrite.All` & `User.Read.All` permissions for Flow 2. Only the part "First Step: Register an application in Azure Active Directory" is what you should follow (with the right - above mentioned - permissions of course).  
 
[[Link to the blog]](https://office365itpros.com/2019/10/03/combining-microsoft-graph-flow-better-office-365-admin/)

To use the Flows below, make sure to import them into Power Automate and replace the variables on the top of the Flows. The values that need to be replaced are clearly marked with `[REPLACE-WITH-*]` where * is the thing you need to replace it with.

## Graph API Flow 1 - Invite External User
This Flow will enable you to invite external users to your Azure Active Directory through Power Automate. It starts with a Flow Button, but I encourage you to use this in a different scenario. It's mostly to show you how it's done. In production scenarios I would use it after someone requests access for an external user. So make sure to try and use this with Microsoft Forms or other scenarios.
[]()

## Graph API Flow 2 - Create Team
This Flow enables you to create a Microsoft Team on request. You can of course copy and paste this into your own process for Teams creation.