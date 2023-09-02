## Azure management group vs Azure subsctiption vs Azure AD tenant
People often gets confused by the hierarchy of Azure management group, Azure Tenant, Azure AD and Azure Subscription.
Let my simplify it.
<br />
When an Azure account is created, it automatically generates one root management group and one Azure Active Directory tenant by default.

#### Management group vs subscriptions
- More than one management group can be created under single management group.
- More than one subscription can be associated to single management group.
- Single subscription cannot simultaneously be associated to more than one management group.

![compare-group-subs](./media/compare-group-with-sub1.png)
<img src="./media/compare-group-with-sub1.png" alt="drawing" style="width:200px;"/>
#### Azure AD tenant vs subscription. 
- More than one subscription can be associated to one Azure AD tenant.
- But one subscription cannot be associated to more than one AD tenant.
![compare-tenatn-subs](./media/compare-tenant-subs.png)

#### Azure AD tenant vs management group
It's important to clarify that while multiple subscriptions can be associated with one Azure AD tenant, there is no direct or inherent relationship between Azure Management Groups and Azure AD tenants.

#### AD users vs Azure AD tenant
In Azure Active directory, one user become a member of one AD tenant which termed as home tenant and the same user can be invited as a guest user to other AD tenants but cannot be direct membership to multiple AD tenants. 

#### Best practice
All subscription in single management group must trust one AD tenant better management, though multiple subscription across management groups could be linked to one Azure AD tenant.

![group-vs-subs](./media/azuregroup-vs-subs.png)

![subs-vs-ad](./media/azure-ad-vs-subs.png)