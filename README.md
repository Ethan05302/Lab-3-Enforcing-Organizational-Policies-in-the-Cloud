# Azure Policy Lab – MapleTech Secure Foundation

## Overview
This lab demonstrates the creation and enforcement of Azure governance policies for a fictional company, MapleTech Solutions. As a Cloud Security Engineer, I created a policy initiative to lock down resources and enforce compliance.

## Policies Created
1. **Only-CanadaCentral**: Denies deployment to regions other than Canada Central.
2. **Require-ProjectName-Tag**: Denies deployment if the 'ProjectName' tag is missing.
3. **Deny-Public-IP**: Prevents creation of public IP addresses.

These were grouped into an initiative called **MapleTech Secure Foundation** and assigned to a resource group in enforce mode.

## Test Results
| Scenario | Result |
|----------|--------|
| Deploy VM in East US |  Denied |
| Deploy storage without tag | Denied |
| Create public IP | Denied |
| Deploy VM in Canada Central with tag | Allowed |

Screenshots are available in the `/screenshots` folder.

## Challenges and Lessons Learned
- Azure Policy provides fine-grained control over resource governance.
- Disabling Public IP during VM creation is necessary to pass network security policies.
- Tag requirements help enforce cost tracking and project ownership.
- Region lock ensures data residency compliance with Canadian regulations.



## Vedio Link: https://youtu.be/BabjxW0t-R8
