# Authentication and Authorization Explained

**Should users be allowed to delete other users with just authentication?**

Before answering this question let’s take a step back to understand what authentication and authorization are and their various use cases when securing applications.  

Authentication and Authorization are utilized in data security, allowing the safeguarding of an automated data system. Both are crucial topics often associated with the internet as key components of its service infrastructure. However, each term is distinct, representing different concepts. While they are frequently used in the same context with the same tools, they are entirely distinct from one another.  

**Authentication**

Authentication in straightforward terms is a medium by which developers know who is using their software. Developers can’t stand behind their applications 24/7 to ensure the requests made to their applications are made by valid users. They come around this by developing mechanisms to enable their app to know exactly the user and interact with it. Applications that have recommendation algorithms take advantage of the ability to authenticate users. They store stats on a particular user and then when the same user is authenticated, they retrieve the previously stored stats and use that to influence the application’s algorithm to result in a personalized experience cherished by users.  

Login and Sign up is arguably the most common form of authentication. When you create an account for the first time, they ask for maybe your name, username, email and so on depending on the requirements of the application you are using. If this action is successful, you can log in with your correct details, you will most likely be redirected to a welcome page. The whole idea of giving credentials and verifying is what authentication entails.  
There are various methods of authentication namely:  
- **Something you know (aka knowledge factors):** This is the most common authentication factor. It verifies identity by confirming users through confidential information they have, such as a login and password.  
- **Something you have (aka possession factors):** Users verify their identity with a unique object such as an access card or key fob. This authentication removes the risk of forgetting passwords; however, it means the user must have the object with them whenever they need to access a system, and they run the risk of losing it by accident or theft.  
- **Something you are (aka inherence factors):** An inherence factor verifies identity through inherent biometric characteristics of the user—like a fingerprint, voice, or iris pattern. The advantage of biometric authentication is that they’re harder to lose or replicate. However, they can be expensive and less accurate than traditional authentication factors.


![Authentication vs Authorization](https://media.geeksforgeeks.org/wp-content/uploads/20190606141632/Untitled-Diagram-2019-06-06T141540.818.png)

**Authorization**  

Authorization is the process of giving someone the ability to access a resource. To explain this effectively take for example a house. The owners of the home can be likened to the owners of sites or applications that authorize you and me daily. We can see authentication as the key to enter the house, however, authorization is limiting the user that entered into the house to only certain parts of the house.  

**Authorization Use Case**  
Consider a collaboration tool like Google Docs.  
The application allows you to create and share documents. Other permissions include being able to update, delete, and comment on a document. If you are the owner of a document, you can share it with someone else and define one or more access policies. For example, you can share your document with someone by letting them just add comments.  

In this scenario:  
- **Resource:** it’s the document  
- **Resource Owner:** this is the user that creates a document, the owner of the document  
- **Authorized User:** the user who is given comment rights by the Resource Owner  

The following diagram represents the authorization to resource access:

![Authentication vs Authorization](https://images.ctfassets.net/kbkgmx9upatd/4ahsyxBLrwLdhPuQ6dia8z/6ac8eed02315eb774b1dbd11d56e0737/authorization-process-diagram.png)

**Authorization Strategies**  
There are several different authorization strategies that computer systems leverage during application deployment. The most prominent ones are Role-Based Access Control (RBAC) and Attribute-Based Access Control (ABAC).  

**Attribute-Based Access Control (ABAC) and Authorization**  
When using ABAC, a computer system defines whether a user has sufficient access privileges to execute an action based on a trait (attribute or claim) associated with that user. An example use case of this authorization process is an online store that sells alcoholic beverages. A user of the online store needs to register and provide proof of their age. In the authorization context, this scenario can be described as follows:  
- The online store is the resource owner  
- Alcoholic beverage is the resource  
- The age of the consumer validated during the registration process is a claim, that is proof of the user’s age attribute  

Presenting the age claim allows the store to process access requests to buy alcohol. So, in this case, the decision to grant access to the resource is made upon the user attribute.  

**Role-Based Access Control (RBAC) and Authorization**  
RBAC, on the other hand, treats authorization as permissions associated with roles and not directly with users. A role is nothing but a collection of permissions. For example, imagine that you work as a department manager in an organization. In this situation, you should have permissions that reflect your role, for example, the ability to approve vacation requests and expense requests, assign tasks, and so on. To grant these permissions, a system manager would first create a role called "Manager" (or similar). Then, they would assign these permissions to this role and would associate you with the "Manager" role. Of course, other users that need the same set of permissions can be associated with that role.  

The advantage of using RBAC is that managing authorization privileges becomes easier because system managers can deal with users and permissions in bulk instead of having to deal with them one by one.  


Now for the very much-awaited answer to:  
**Should users be allowed to delete other users with just authentication?**  
The answer would be NO. The reason being, that if a user is permitted to delete another user, a user could wake up one morning and decide to delete the entire users registered with an organization.  


Imagine how catastrophic that would be for companies that process transactions and manage how much a user deposits, withdraws, personalization data, and so many other things you could imagine. So you get why these concepts aren’t taken lightly in the software engineering industry. I hope you enjoyed this read. 
**Follow for more !!!**

**References**

Geeks for Geeks

strongdm.com

auth0.com

earn.stackup.dev


**Author**: Fadehan Daniel (Fadex)

