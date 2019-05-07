# ![LOGO](logo.png) StorageManagementClient **flow**ground Connector

## Description

A generated **flow**ground connector for the StorageManagementClient API (version 2018-07-01).

Generated from: https://api.apis.guru/v2/specs/azure.com/storage/2018-07-01/swagger.json<br/>
Generated at: 2019-05-07T17:39:16+03:00

## API Description

The Azure Storage Management API.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Lists all of the available Storage Rest API operations.

*Tags:* `Operations`

#### Input Parameters
* `api-version` - _required_ - The API version to use for this operation.

### Checks that the storage account name is valid and is not already in use.

*Tags:* `StorageAccounts`

#### Input Parameters
* `api-version` - _required_ - The API version to use for this operation.
* `subscriptionId` - _required_ - The ID of the target subscription.

### Gets the current usage count and the limit for the resources of the location under the subscription.

*Tags:* `LocationUsage`

#### Input Parameters
* `api-version` - _required_ - The API version to use for this operation.
* `subscriptionId` - _required_ - The ID of the target subscription.
* `location` - _required_ - The location of the Azure Storage resource.

### Lists the available SKUs supported by Microsoft.Storage for given subscription.

*Tags:* `Skus`

#### Input Parameters
* `api-version` - _required_ - The API version to use for this operation.
* `subscriptionId` - _required_ - The ID of the target subscription.

### Lists all the storage accounts available under the subscription. Note that storage keys are not returned; use the ListKeys operation for this.

*Tags:* `StorageAccounts`

#### Input Parameters
* `api-version` - _required_ - The API version to use for this operation.
* `subscriptionId` - _required_ - The ID of the target subscription.

### Lists all the storage accounts available under the given resource group. Note that storage keys are not returned; use the ListKeys operation for this.

*Tags:* `StorageAccounts`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group within the user's subscription. The name is case insensitive.
* `api-version` - _required_ - The API version to use for this operation.
* `subscriptionId` - _required_ - The ID of the target subscription.

### Deletes a storage account in Microsoft Azure.

*Tags:* `StorageAccounts`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group within the user's subscription. The name is case insensitive.
* `accountName` - _required_ - The name of the storage account within the specified resource group. Storage account names must be between 3 and 24 characters in length and use numbers and lower-case letters only.
* `api-version` - _required_ - The API version to use for this operation.
* `subscriptionId` - _required_ - The ID of the target subscription.

### Returns the properties for the specified storage account including but not limited to name, SKU name, location, and account status. The ListKeys operation should be used to retrieve storage keys.

*Tags:* `StorageAccounts`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group within the user's subscription. The name is case insensitive.
* `accountName` - _required_ - The name of the storage account within the specified resource group. Storage account names must be between 3 and 24 characters in length and use numbers and lower-case letters only.
* `api-version` - _required_ - The API version to use for this operation.
* `subscriptionId` - _required_ - The ID of the target subscription.
* `$expand` - _optional_ - May be used to expand the properties within account's properties. By default, data is not included when fetching properties. Currently we only support geoReplicationStats.
    Possible values: geoReplicationStats.

### The update operation can be used to update the SKU, encryption, access tier, or tags for a storage account. It can also be used to map the account to a custom domain. Only one custom domain is supported per storage account; the replacement/change of custom domain is not supported. In order to replace an old custom domain, the old value must be cleared/unregistered before a new value can be set. The update of multiple properties is supported. This call does not change the storage keys for the account. If you want to change the storage account keys, use the regenerate keys operation. The location and name of the storage account cannot be changed after creation.

*Tags:* `StorageAccounts`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group within the user's subscription. The name is case insensitive.
* `accountName` - _required_ - The name of the storage account within the specified resource group. Storage account names must be between 3 and 24 characters in length and use numbers and lower-case letters only.
* `api-version` - _required_ - The API version to use for this operation.
* `subscriptionId` - _required_ - The ID of the target subscription.

### Asynchronously creates a new storage account with the specified parameters. If an account is already created and a subsequent create request is issued with different properties, the account properties will be updated. If an account is already created and a subsequent create or update request is issued with the exact same set of properties, the request will succeed.

*Tags:* `StorageAccounts`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group within the user's subscription. The name is case insensitive.
* `accountName` - _required_ - The name of the storage account within the specified resource group. Storage account names must be between 3 and 24 characters in length and use numbers and lower-case letters only.
* `api-version` - _required_ - The API version to use for this operation.
* `subscriptionId` - _required_ - The ID of the target subscription.

### List SAS credentials of a storage account.

*Tags:* `StorageAccounts`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group within the user's subscription. The name is case insensitive.
* `accountName` - _required_ - The name of the storage account within the specified resource group. Storage account names must be between 3 and 24 characters in length and use numbers and lower-case letters only.
* `api-version` - _required_ - The API version to use for this operation.
* `subscriptionId` - _required_ - The ID of the target subscription.

### List service SAS credentials of a specific resource.

*Tags:* `StorageAccounts`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group within the user's subscription. The name is case insensitive.
* `accountName` - _required_ - The name of the storage account within the specified resource group. Storage account names must be between 3 and 24 characters in length and use numbers and lower-case letters only.
* `api-version` - _required_ - The API version to use for this operation.
* `subscriptionId` - _required_ - The ID of the target subscription.

### Failover request can be triggered for a storage account in case of availability issues. The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts. The secondary cluster will become primary after failover.

*Tags:* `StorageAccounts`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group within the user's subscription. The name is case insensitive.
* `accountName` - _required_ - The name of the storage account within the specified resource group. Storage account names must be between 3 and 24 characters in length and use numbers and lower-case letters only.
* `api-version` - _required_ - The API version to use for this operation.
* `subscriptionId` - _required_ - The ID of the target subscription.

### Lists the access keys for the specified storage account.

*Tags:* `StorageAccounts`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group within the user's subscription. The name is case insensitive.
* `accountName` - _required_ - The name of the storage account within the specified resource group. Storage account names must be between 3 and 24 characters in length and use numbers and lower-case letters only.
* `api-version` - _required_ - The API version to use for this operation.
* `subscriptionId` - _required_ - The ID of the target subscription.

### Regenerates one of the access keys for the specified storage account.

*Tags:* `StorageAccounts`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group within the user's subscription. The name is case insensitive.
* `accountName` - _required_ - The name of the storage account within the specified resource group. Storage account names must be between 3 and 24 characters in length and use numbers and lower-case letters only.
* `api-version` - _required_ - The API version to use for this operation.
* `subscriptionId` - _required_ - The ID of the target subscription.

## License

**flow**ground :- Telekom iPaaS / azure-com-storage-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
