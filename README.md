# Azure Managed Application for Lighthouse Onboarding and Policy Deployment

This repository contains ARM templates for creating an Azure Managed Application that onboards customers to Azure Lighthouse and deploys specific Azure policies. The solution includes the following components:

- **mainTemplate.json**: The main ARM template that references nested templates.
- **createUiDefinition.json**: Defines the UI elements for user input in the Azure portal.
- **nestedtemplates/marketplaceDelegatedResourceManagement.json**: Template for onboarding to Azure Lighthouse.
- **nestedtemplates/deployPolicies.json**: Template for deploying Azure policies.

## Prerequisites

- An Azure account with the necessary permissions to create resources and deploy policies.
- A subscription ID where the resources will be deployed.

## Deployment

You can deploy this solution to Azure using the following steps:

1. **Clone this repository**:
   ```bash
   git clone https://github.com/yourusername/reponame.git
   cd reponame

2. **Deploy to Azure:**
Click the button below to deploy the solution directly to your Azure subscription.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https://raw.githubusercontent.com/dsvoda/AzureMarketplaceOffer/main/mainTemplate.json)

## Files
- **mainTemplate.json**: Main ARM template.
- **createUiDefinition.json**: UI definition for the Azure portal.
- **nestedtemplates/marketplaceDelegatedResourceManagement.json**: Template for Azure Lighthouse onboarding.
- **nestedtemplates/deployPolicies.json**: Template for deploying policies.

## Parameters
1. **mainTemplate.json**
- customerTenantId: Tenant ID of the customer.
- principalId: Principal ID for Lighthouse.
- roleDefinitionId: Role Definition ID.
- principalIdDisplayName: Display name of the principal ID.
- managedByTenantId: Managed by Tenant ID.
- location: Location for the resources.
- subscriptionId: Subscription ID where the policies will be deployed.
- allowedLocations: List of allowed locations for resources.
- allowedVmSizes: List of allowed VM sizes for virtual machines.
2. **createUiDefinition.json**
- customerTenantId: Tenant ID of the customer.
- principalId: Principal ID for Lighthouse.
- roleDefinitionId: Role Definition ID.
- principalIdDisplayName: Display name of the principal ID.
- managedByTenantId: Managed by Tenant ID.
- location: Location for the resources.
- subscriptionId: Subscription ID where the policies will be deployed.
- allowedLocations: List of allowed locations for resources.
- allowedVmSizes: List of allowed VM sizes for virtual machines.

## Contributing
If you would like to contribute to this repository, please fork the repo and create a pull request. We welcome all contributions.
