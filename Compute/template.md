---
title: Resiliency Recommendations for AZURE SERVICE NAME
description: Best practices and recommendations for AZURE SERVICE NAME and associated resources.
author: rosanto
ms.author: rosanto
ms.date: 03/14/2023
ms.topic: conceptual
ms.service: architecture-center
ms.subservice: well-architected
ms.custom:
  - recommendations
products:
  - azure, AZURE SERVICE NAME
categories:
  - administration, resiliency, performance, reliability, operational excellence
---

# AZURE SERVICE NAME

The presented recommendations in this guidance include AZURE SERVICE NAME, and associated AZURE SERVICE NAME settings.

### ID-1 - Recommendation Title

**Importance:** P4 (0 to 4)

**Best Practices Guidance:**
- Brief description why this is important.

**Read more:**
- [Link Title](https://url)

**Azure Resource Graph query:**

Use the following query to identify resources that are not compliant:

```kusto
Resources
| project name, location, type
| where type =~ 'Microsoft.Compute/virtualMachines'
| order by name desc
```

<br>

### ID-2 - Recommendation Title

**Importance:** P4 (0 to 4)

**Best Practices Guidance:**
- Brief description why this is important.

**Read more:**
- [Link Title](https://url)

**Azure Resource Graph query:**

Use the following query to identify resources that are not compliant:

```kusto
Resources
| project name, location, type
| where type =~ 'Microsoft.Compute/virtualMachines'
| order by name desc
```

<br>