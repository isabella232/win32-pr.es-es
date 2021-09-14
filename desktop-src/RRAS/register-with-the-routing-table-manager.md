---
title: Registro con el Administrador de tablas de enrutamiento
description: El código de ejemplo siguiente muestra cómo registrar una nueva entidad con el administrador de tablas de enrutamiento.
ms.assetid: 320cc97f-2875-4d26-b2f4-5611a43d5839
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b5e2f3ba3df414f383305d09c129b52bcb32cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069164"
---
# <a name="register-with-the-routing-table-manager"></a>Registro con el Administrador de tablas de enrutamiento

El código de ejemplo siguiente muestra cómo registrar una nueva entidad con el administrador de tablas de enrutamiento.


```C++
#include <windows.h>
#include <stdio.h>
#include "Rtmv2.h"
#include "nldef.h"

// The following #defines are from routprot.h in the Platform Software Develoment Kit (SDK)
#define PROTO_TYPE_UCAST     0
#define PROTOCOL_ID(Type, VendorId, ProtocolId) (((Type & 0x03)<<30)|((VendorId & 0x3FFF)<<16)|(ProtocolId & 0xFFFF))
#define PROTO_VENDOR_ID      0xFFFF

int __cdecl main(){
 
    RTM_ENTITY_HANDLE RtmRegHandle;
    RTM_ENTITY_INFO EntityInfo;
    RTM_REGN_PROFILE RegnProfile;
    DWORD dwRet = ERROR_SUCCESS;

    EntityInfo.RtmInstanceId = 0;
    EntityInfo.AddressFamily = AF_INET;
    EntityInfo.EntityId.EntityProtocolId = PROTO_IP_RIP;
    EntityInfo.EntityId.EntityInstanceId = PROTOCOL_ID(PROTO_TYPE_UCAST, PROTO_VENDOR_ID, PROTO_IP_RIP);

    // Register the new entity
    dwRet = RtmRegisterEntity(&EntityInfo, NULL, NULL, FALSE, &RegnProfile, &RtmRegHandle);
    if (dwRet != ERROR_SUCCESS){
        // Registration failed - Log an Error and Quit
    }

    // Clean-up: Deregister the new entity
    dwRet = RtmDeregisterEntity(RtmRegHandle);
    if (dwRet != ERROR_SUCCESS){
        // Registration failed - Log an Error and Quit
    }

    return 0;
}
```



 

 




