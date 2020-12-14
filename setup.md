# Adaptive Application Controls

[#3125 Use Only Secured Applications](https://nodesource.com/products/nsolid)

[POC Documentation](https://travis-ci.org/joemccann/dillinger)

Adaptive application controls are an intelligent and automated solution for defining allow lists of known-safe applications for your machines.
`steps`
  - enable and configure adaptive application controls.
  - Security Center detects applications running in machines created and segregates machines to configured/recommended/no recommendations.
  - sends security alerts if any application runs other than the ones you've defined as safe [see in](#in-brief)
  
  
  
  This article shows how to delete resource groups and resources. It describes how Azure Resource Manager orders the deletion of resources when you delete a resource group.

How order of deletion is determined
When you delete a resource group, Resource Manager determines the order to delete resources. It uses the following order:

All the child (nested) resources are deleted.

Resources that manage other resources are deleted next. A resource can have the managedBy property set to indicate that a different resource manages it. When this property is set, the resource that manages the other resource is deleted before the other resources.

The remaining resources are deleted after the previous two categories.

After the order is determined, Resource Manager issues a DELETE operation for each resource. It waits for any dependencies to finish before proceeding.

For synchronous operations, the expected successful response codes are:

200
204
404
For asynchronous operations, the expected successful response is 202. Resource Manager tracks the location header or the azure-async operation header to determine the status of the asynchronous delete operation.

Deletion errors
When a delete operation returns an error, Resource Manager retries the DELETE call. Retries happen for the 5xx, 429 and 408 status codes. By default, the time period for retry is 15 minutes.

After deletion
  
### In Brief

