---
description: La directiva LSA proporciona varias funciones que puede usar para crear, enumerar y eliminar dominios de confianza y para establecer y recuperar información de dominio de confianza.
ms.assetid: 0c7534d7-3372-49c4-992c-9b519279982d
title: Administración de información de dominio de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7df297b8c83ebe9054ca6f04b657905c21fae6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073602"
---
# <a name="managing-trusted-domain-information"></a>Administración de información de dominio de confianza

La directiva LSA proporciona varias funciones que puede usar para crear, enumerar y eliminar dominios de confianza y para establecer y recuperar información de dominio de confianza.

Para poder administrar información de dominio de confianza, la aplicación debe obtener un identificador para un objeto [**Policy,**](policy-object.md) como se explica en Apertura de un [identificador de objeto de directiva.](opening-a-policy-object-handle.md)

Puede enumerar los dominios de confianza llamando a [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).

Para recuperar información sobre un dominio de confianza, llame a [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) o [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname). Ambas funciones devuelven la misma información; sin embargo, **LsaQueryTrustedDomainInfo** identifica el dominio de confianza por SID y **LsaQueryTrustedDomainInfoByName** identifica el dominio de confianza por nombre.

Para establecer información para un dominio de confianza, llame a [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) o [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname). Al igual que con las funciones de consulta, **LsaSetTrustedDomainInformation** identifica el dominio de confianza por SID, mientras **que LsaSetTrustedDomainInfoByName** identifica el dominio de confianza por nombre.

La aplicación puede revocar una relación de confianza para un dominio de confianza llamando a [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain).

En el ejemplo siguiente se enumeran los dominios de confianza para el sistema local.


```C++
#include <windows.h>

void EnumerateTrusts(LSA_HANDLE PolicyHandle)
{
  LSA_ENUMERATION_HANDLE hEnum=0; 
  PLSA_TRUST_INFORMATION TrustInfo = NULL;
  ULONG ulReturned = 0;               
  NTSTATUS Status = 0;
  ULONG i;
  WCHAR StringBuffer[256];

  // Enumerate the trusted domains until there are no more to return.
  do 
  {
    Status = LsaEnumerateTrustedDomains(
       PolicyHandle,         // an open policy handle
       &hEnum,               // enumeration tracker
       (PVOID*)&TrustInfo,   // buffer to receive data
       32000,                // recommended buffer size
       &ulReturned           // number of items returned in TrustInfo
    );

    // Check the return status for errors.
    if((Status != STATUS_SUCCESS) &&
       (Status != STATUS_MORE_ENTRIES) &&
     (Status != STATUS_NO_MORE_ENTRIES))
      {
        // Handle the error.
        wprintf(L"Error occurred enumerating domains %lu\n",
        LsaNtStatusToWinError(Status));
        return;
      } 

      wprintf(L"Status %lu\n", LsaNtStatusToWinError(Status));
      // Process the trusted domain information.
      for (i=0;i<ulReturned; i++) 
      {
        // LSA_Unicode strings might not be null-terminated.
        if(TrustInfo[i].Name.Length < 256)
        {
            wcsncpy_s(StringBuffer,
                256,
                TrustInfo[i].Name.Buffer,
                TrustInfo[i].Name.Length
            );
            // Guarantee that StringBuffer is null-terminated.
            StringBuffer[TrustInfo[i].Name.Length] = NULL; 
        }
        else
        {
            fprintf(stderr, "Name too long for string buffer.\n");
            exit(1);
        }
        
        wprintf(L"Enum Trusted Domain - %ws ", StringBuffer);
      }
      // Free the buffer.
      if (TrustInfo != NULL) 
      {
        LsaFreeMemory(TrustInfo);
        TrustInfo = NULL;
      }
    } while (Status != STATUS_NO_MORE_ENTRIES);
    return;
}
```



 

 



