---
title: "Modem API Summary2 | Microsoft Docs"
ms.custom: ""
ms.date: "11/30/2017"
ms.prod: "host-integration-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 13f42b3b-9ced-42b8-be10-b52b8d949b06
caps.latest.revision: 3
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Modem API Summary
To simplify the task for independent hardware vendors (IHVs) who want to use this feature, four new entry points have been added to SNALINK.DLL. An IHV who uses these must be linking with IHVLINK.LIB, a stub library that contains the exports library for SNALINK.DLL. This API enables the IHV to simply maintain the contents of a [MODEM_STATUS](../HIS2010/modem-status2.md) structure. The underlying SNALINK library code handles the communication of this information to the modem lights application.  
  
 The modem status functions are as follows.  
  
|Function|Description|  
|--------------|-----------------|  
|[SNAModemInitialize](../HIS2010/snamodeminitialize1.md)|Initializes the communication path to the SNA Modem application.|  
|[SNAModemAddLink](../HIS2010/snamodemaddlink2.md)|Adds an SNA link.|  
|[SNAModemDeleteLink](../HIS2010/snamodemdeletelink1.md)|Deletes the resources associated with a link.|  
|[SNAModemTerminate](../HIS2010/snamodemterminate2.md)|Terminates an SNA link.|