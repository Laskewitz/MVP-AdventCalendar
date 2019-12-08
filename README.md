# MVP Advent Calendar
Welcome to the gift I have prepared for you for the 9th day of the MVP Advent Calendar. 
Thanks to Megan Walker for the great idea of bringing all the MVPs together for a great advent calendar. 

![Advent Calendar](/Advent.png)

I hope you enjoy it!

## Create an Azure AD App with Graph API permissions
To use these Flows successfully you should create an Azure AD App. My colleague Gustavo Velez wrote a very good blog about how to create this. He uses the `SecurityEvents.Read.All` permissions, which we are not gonna use. Use the following permissions for the different Flows:
 
 | Flow Name | Graph API Permissions |
 |:-------------:|:-------------:|
 | Graph API Flow 1 - Invite External User | `User.Invite.All` |
 | Graph API Flow 2 - Create Team | `Group.ReadWrite.All` & `User.Read.All` |  

Only the part "First Step: Register an application in Azure Active Directory" is what you should follow (with the right - above mentioned - permissions of course).  
 
[[Link to the blog]](https://office365itpros.com/2019/10/03/combining-microsoft-graph-flow-better-office-365-admin/)

To use the Flows below, make sure to import them into Power Automate and replace the variables on the top of the Flows. The values that need to be replaced are clearly marked with `[REPLACE-WITH-*]` where * is the thing you need to replace it with.

## Graph API Flow 1 - Invite External User
This Flow will enable you to invite external users to your Azure Active Directory through Power Automate. It starts with a Flow Button, but I encourage you to use this in a different scenario. It's mostly to show you how it's done. In production scenarios I would use it after someone requests access for an external user. So make sure to try and use this with Microsoft Forms or other scenarios.

### Used Graph API calls
* [Create Invitation](https://docs.microsoft.com/en-us/graph/api/invitation-post?view=graph-rest-1.0&tabs=http)

## Graph API Flow 2 - Create Team
This Flow enables you to create a Microsoft Team on request. You can of course copy and paste this into your own process for Teams creation. 

### Used Graph API calls
* [Create Group](https://docs.microsoft.com/en-us/graph/api/group-post-groups?view=graph-rest-1.0&tabs=http)
* [Get User](https://docs.microsoft.com/en-us/graph/api/user-get?view=graph-rest-1.0&tabs=http)
* [Add Group Owner](https://docs.microsoft.com/en-us/graph/api/group-post-owners?view=graph-rest-1.0&tabs=http)
* [Add Group Member](https://docs.microsoft.com/en-us/graph/api/group-post-members?view=graph-rest-1.0&tabs=http)
* [Create Team](https://docs.microsoft.com/en-us/graph/api/team-put-teams?view=graph-rest-1.0&tabs=http)
 