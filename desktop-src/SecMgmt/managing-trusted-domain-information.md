---
description: La Directiva de LSA proporciona varias funciones que se pueden usar para crear, enumerar y eliminar dominios de confianza, así como para establecer y recuperar información de dominio de confianza.
ms.assetid: 0c7534d7-3372-49c4-992c-9b519279982d
title: Administrar información de dominios de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7df297b8c83ebe9054ca6f04b657905c21fae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278422"
---
# <a name="managing-trusted-domain-information"></a><span data-ttu-id="36fb0-103">Administrar información de dominios de confianza</span><span class="sxs-lookup"><span data-stu-id="36fb0-103">Managing Trusted Domain Information</span></span>

<span data-ttu-id="36fb0-104">La Directiva de LSA proporciona varias funciones que se pueden usar para crear, enumerar y eliminar dominios de confianza, así como para establecer y recuperar información de dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="36fb0-104">LSA Policy provides several functions that you can use to create, enumerate, and delete trusted domains and to set and retrieve trusted domain information.</span></span>

<span data-ttu-id="36fb0-105">Antes de poder administrar la información del dominio de confianza, la aplicación debe obtener un identificador de un objeto de [**Directiva**](policy-object.md) , tal como se explica en [abrir un identificador de objeto de directiva](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="36fb0-105">Before you can manage trusted domain information, your application must get a handle to a [**Policy**](policy-object.md) object, as explained in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="36fb0-106">Puede enumerar los dominios de confianza mediante una llamada a [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span><span class="sxs-lookup"><span data-stu-id="36fb0-106">You can enumerate the trusted domains by calling [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span></span>

<span data-ttu-id="36fb0-107">Para recuperar información sobre un dominio de confianza, llame a [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) o [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname).</span><span class="sxs-lookup"><span data-stu-id="36fb0-107">To retrieve information about a trusted domain, call either [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) or [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname).</span></span> <span data-ttu-id="36fb0-108">Ambas funciones devuelven la misma información; sin embargo, **LsaQueryTrustedDomainInfo** identifica el dominio de confianza por SID y **LsaQueryTrustedDomainInfoByName** identifica el dominio de confianza por nombre.</span><span class="sxs-lookup"><span data-stu-id="36fb0-108">Both functions return the same information; however, **LsaQueryTrustedDomainInfo** identifies the trusted domain by SID, and **LsaQueryTrustedDomainInfoByName** identifies the trusted domain by name.</span></span>

<span data-ttu-id="36fb0-109">Para establecer la información de un dominio de confianza, llame a [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) o [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname).</span><span class="sxs-lookup"><span data-stu-id="36fb0-109">To set information for a trusted domain, call either [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) or [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname).</span></span> <span data-ttu-id="36fb0-110">Al igual que con las funciones de consulta, **LsaSetTrustedDomainInformation** identifica el dominio de confianza por SID, mientras que **LsaSetTrustedDomainInfoByName** identifica el dominio de confianza por nombre.</span><span class="sxs-lookup"><span data-stu-id="36fb0-110">As with the query functions, **LsaSetTrustedDomainInformation** identifies the trusted domain by SID, while **LsaSetTrustedDomainInfoByName** identifies the trusted domain by name.</span></span>

<span data-ttu-id="36fb0-111">La aplicación puede revocar una relación de confianza para un dominio de confianza mediante una llamada a [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain).</span><span class="sxs-lookup"><span data-stu-id="36fb0-111">Your application can revoke a trust relationship for a trusted domain by calling [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain).</span></span>

<span data-ttu-id="36fb0-112">En el ejemplo siguiente se enumeran los dominios de confianza para el sistema local.</span><span class="sxs-lookup"><span data-stu-id="36fb0-112">The following example enumerates the trusted domains for the local system.</span></span>


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



 

 



