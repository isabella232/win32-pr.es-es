---
title: Rellenar condiciones de filtro
description: El código de ejemplo siguiente muestra cómo rellenar las condiciones de filtro que usa una aplicación de servidor para buscar filtros y eventos que le afecten.
ms.assetid: 6c7c8d55-2cd4-45fe-ad6b-e568941d6765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5f66f2cb3eaa28036e4861ba42397eb371dd73f8d15452fb172e957809105f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068835"
---
# <a name="populating-filter-conditions"></a>Rellenar condiciones de filtro

En el código de ejemplo siguiente se muestra cómo rellenar las condiciones de filtro usadas por una aplicación de servidor para buscar filtros y eventos que le afecten.

> [!Note]  
> Estas condiciones son las mismas que las admitidas por la API **IsPortAllowed de nivel** inferior.

 


```C++
DWORD InitFilterConditions(
         __in_opt PCWSTR appPath,
         __in_opt const SOCKADDR* localAddr,
         __in_opt UINT8 ipProtocol,
         __in UINT32 numCondsIn,
         __out_ecount_part(numCondsIn, *numCondsOut)
            FWPM_FILTER_CONDITION0* conds,
         __out UINT32* numCondsOut,
         __deref_out FWP_BYTE_BLOB** appId
         )
{
   DWORD result = NO_ERROR;
   UINT32 numConds = 0;
   UINT16 port;
   void* addr;

   *numCondsOut = 0;

   if (localAddr != NULL)
   {
      port = INETADDR_PORT(localAddr);
      if (port != 0)
      {
         if (numConds >= numCondsIn)
         {
            result = ERROR_INSUFFICIENT_BUFFER;
            goto CLEANUP;
         }

         conds[numConds].fieldKey = FWPM_CONDITION_IP_LOCAL_PORT;
         conds[numConds].matchType = FWP_MATCH_EQUAL;
         conds[numConds].conditionValue.type = FWP_UINT16;
         // The SOCKADDR struct has the port in network order, but the
         // filtering engine expects it in host order.
         conds[numConds].conditionValue.uint16 = ntohs(port);
         ++numConds;
      }

      if (!INETADDR_ISANY(localAddr))
      {
         if (numConds > numCondsIn)
         {
            result = ERROR_INSUFFICIENT_BUFFER;
            goto CLEANUP;
         }

         addr = INETADDR_ADDRESS(localAddr);

         conds[numConds].fieldKey = FWPM_CONDITION_IP_LOCAL_ADDRESS;
         conds[numConds].matchType = FWP_MATCH_EQUAL;

         if (localAddr->sa_family == AF_INET)
         {
            conds[numConds].conditionValue.type = FWP_UINT32;
            // The SOCKADDR struct has the port in network order, but the
            // filtering engine expects it in host order.
            conds[numConds].conditionValue.uint32 = ntohl(*(ULONG*)addr);
         }
         else
         {
            conds[numConds].conditionValue.type = FWP_BYTE_ARRAY16_TYPE;
            conds[numConds].conditionValue.byteArray16 =
               (FWP_BYTE_ARRAY16*)addr;
         }

         ++numConds;
      }
   }

   if (ipProtocol != 0)
   {
      if (numConds >= numCondsIn)
      {
         result = ERROR_INSUFFICIENT_BUFFER;
         goto CLEANUP;
      }

      conds[numConds].fieldKey = FWPM_CONDITION_IP_PROTOCOL;
      conds[numConds].matchType = FWP_MATCH_EQUAL;
      conds[numConds].conditionValue.type = FWP_UINT8;
      conds[numConds].conditionValue.uint8 = ipProtocol;
      ++numConds;
   }

   if (appPath != NULL)
   {
      if (numConds >= numCondsIn)
      {
         result = ERROR_INSUFFICIENT_BUFFER;
         goto CLEANUP;
      }

      // appPath must be a fully-qualified file name, and the file must
      // exist on the local machine.
      result = FwpmGetAppIdFromFileName0(appPath, appId);
      BAIL_ON_ERROR(FwpmGetAppIdFromFileName0);

      conds[numConds].fieldKey = FWPM_CONDITION_ALE_APP_ID;
      conds[numConds].matchType = FWP_MATCH_EQUAL;
      conds[numConds].conditionValue.type = FWP_BYTE_BLOB_TYPE;
      conds[numConds].conditionValue.byteBlob = *appId;
      ++numConds;
   }

   *numCondsOut = numConds;

CLEANUP:
   return result;
}
```



 

 




