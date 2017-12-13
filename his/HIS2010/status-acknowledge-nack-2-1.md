---
title: "Status-Acknowledge(Nack-2)1 | Microsoft Docs"
ms.custom: ""
ms.date: "11/30/2017"
ms.prod: "host-integration-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d61cf220-d8dd-455f-b61a-c760b24b64c4
caps.latest.revision: 3
---
# Status-Acknowledge(Nack-2)
The **Status-Acknowledge(Nack-2)** message flows from the node to the application. It is used with both system services control point (SSCP) and primary logical unit (PLU) connections.  
  
## Syntax  
  
```  
  
struct Status-Acknowledge(Nack-2) {  
    PTRBFHDR  nxtqptr;  
    PTRBFELT  hdreptr;  
    CHAR      numelts;  
    CHAR      msgtype;  
    CHAR      srcl;  
    CHAR      srcp;  
    INTEGER   srci;  
    CHAR      destl;  
    CHAR      destp;  
    INTEGER   desti;  
    CHAR      sfhdr.stackhdr.akstat;  
    CHAR      sfhdr.stackhdr.akqual;  
    INTEGER   sfhdr.stackhdr.akmsgkey;  
    CHAR      sfhdr.stackhdr.akflags1;  
    CHAR sfhdr.stackhdr.akflags2;  
    INTEGER sfhdr.stackhdr.aknumb1;  
    INTEGER sfhdr.stackhdr.aknumb2;  
};   
```  
  
## Members  
 *nxtqptr*  
 Pointer to next buffer header.  
  
 *hdreptr*  
 Pointer to buffer element (NIL).  
  
 *numelts*  
 Number of buffer elements (0x00).  
  
 *msgtype*  
 Message type STATFMI (0x21).  
  
 *srcl*  
 Source locality.  
  
 *srcp*  
 Source partner.  
  
 *srci*  
 Source index.  
  
 *destl*  
 Destination locality.  
  
 *destp*  
 Destination partner.  
  
 *desti*  
 Destination index.  
  
 *sfhdr.stackhdr.akstat*  
 Status type ACK (0x01).  
  
 *sfhdr.stackhdr.akqual*  
 Acknowledgment type ACKNEG2 (0x04).  
  
 *sfhdr.stackhdr.akmsgkey*  
 Message key.  
  
 *sfhdr.stackhdr.akflags1*  
 Reserved.  
  
 *sfhdr.stackhdr.akflags2*  
 Critical failure indicator.  
  
 Noncritical failure (0x00) Critical failure (0x01)  
  
 *sfhdr.stackhdr.aknumb1*  
 Error code 1.  
  
 *sfhdr.stackhdr.aknumb2*  
 Error code 2.  
  
## Remarks  
  
-   The **Status-Acknowledge(Nack-2)** message consists of a buffer header only. There is no buffer element.  
  
-   The message key refers to the message key in the inbound data message to which this is a negative acknowledgment.  
  
-   For more information about error codes, see [Error and Sense Codes](../HIS2010/error-and-sense-codes1.md).