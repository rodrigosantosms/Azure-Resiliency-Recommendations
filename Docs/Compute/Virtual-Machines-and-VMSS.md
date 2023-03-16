---
title: Resiliency Recommendations for Virtual Machines
description: Best practices and recommendations for Virtual Machines and associated resources.
author: rosanto
ms.author: rosanto
ms.date: 03/14/2023
ms.topic: conceptual
ms.service: architecture-center
ms.subservice: well-architected
ms.custom:
  - recommendations
products:
  - azure, virtual machines, disks, network interfaces
categories:
  - administration, resiliency, performance, reliability, operational excellence
---

# Virtual Machines

The presented recommendations in this guidance include Virtual Machines, Disks, Network Interfaces, and associated Virtual Machine settings.

## Summary of Recommendations and Microsoft Verification/Validation

... Content
| Resource Category | Service Name | Recommendation | Verified by Microsoft |
| :--:              | :--:         | :--     | :--:     |
| Compute | Virtual Machines | VM-1 - Avoid running a production workload on a single VM | Y |

### VM-1 - Avoid running a production workload on a single VM

**Importance:** P0

**Best Practices Guidance:**
- A single VM deployment is not resilient to planned or unplanned Azure maintenances. Instead, put multiple VMs in an availability set or virtual machine scale set, with a load balancer in front of them.

**Read more:**
- [Availability options for Azure Virtual Machines](https://learn.microsoft.com/en-us/azure/virtual-machines/availability)

**Azure Resource Graph query:**

Use the following query to identify resources that are not compliant:

```kusto
Resources
| project name, location, type
| where type =~ 'Microsoft.Compute/virtualMachines'
| order by name desc
```

<br>

## VM-2 - Use managed disks for Virtual Machine hard disks

**Importance:** P1

**Best Practices Guidance:**
- Managed disks provide better reliability for VMs in an availability set, because the disks are sufficiently isolated from each other to avoid single points of failure. Also, managed disks aren't subject to the IOPS limits of VHDs created in a storage account.

**Read more:**
- [Azure managed disk types](https://learn.microsoft.com/en-us/azure/virtual-machines/disks-types)

**Azure Resource Graph query:**

Use the following query to identify resources that are not compliant:

```kusto
Resources
| project name, location, type
| where type =~ 'Microsoft.Compute/virtualMachines'
| order by name desc
```
<br>