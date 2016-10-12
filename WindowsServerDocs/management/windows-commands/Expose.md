---
title: Expose
description: "Windows Commands"
ms.custom: na
ms.prod: windows-server-threshold
ms.reviewer: na
ms.suite: na
ms.technology: manage-windows-commands
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9b0a21cf-3bef-4ade-b8f1-ac42f9203947
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/12/2016
---

# Expose

>Applies To: Windows Server&reg; 2016, Windows Server&reg; 2012 R2, Windows Server&reg; 2012

Exposes a persistent shadow copy as a drive letter, share, or mount point.  
  
For examples of how to use this command, see [Examples](#BKMK_examples).  
  
## Syntax  
  
```  
expose <ShadowID> {<Drive:> | <Share> | <MountPoint>}  
```  
  
## Parameters  
  
|Parameter|Description|  
|-------------|---------------|  
|ShadowID|Specifies the shadow ID of the shadow copy you want to expose.|  
|<Drive:>|Exposes the specified shadow copy as a drive letter \(for example, P:\).|  
|<Share>|Exposes the specified shadow copy at a share \(for example, \\\\*MachineName*\\\).|  
|<MountPoint>|Exposes the specified shadow copy to a mount point \(for example, C:\\shadowcopy\\\).|  
  
## Remarks  
  
-   You can use an existing alias or an environment variable in place of *ShadowID*. Use **add** without parameters to see existing aliases.  
  
## <a name="BKMK_examples"></a>Examples  
To expose the persistent shadow copy associated with the VSS\_SHADOW\_1 environment variable as drive X, type:  
  
```  
expose %vss_shadow_1% x:  
```  
  
#### Additional references  
[Command-Line Syntax Key](Command-Line-Syntax-Key.md)  
  
