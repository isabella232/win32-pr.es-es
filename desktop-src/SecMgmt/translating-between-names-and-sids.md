---
description: La autoridad de seguridad local (LSA) proporciona funciones para traducir entre los nombres de usuario, grupo y grupo local y sus valores de identificador de seguridad (SID) correspondientes.
ms.assetid: 8845b709-a8f9-4d0f-a4a6-86d23d6b01d5
title: Traducir entre nombres y SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417034a99331c09f20546f2f352bc762a86f02e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686669"
---
# <a name="translating-between-names-and-sids"></a>Traducir entre nombres y SID

La [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) proporciona funciones para traducir entre los nombres de usuario, grupo y grupo local y sus valores de [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) correspondientes. Para buscar nombres de cuenta, llame a la función [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) . Esta función devuelve el SID como un par de índice de dominio o RID. Para obtener el SID como un solo elemento, llame a la función [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) . Para buscar los SID, llame a [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).

Estas funciones pueden convertir la información de nombre y SID de cualquier dominio de confianza del sistema local.

Antes de poder traducir entre nombres de cuenta y Sid, la aplicación debe obtener un identificador para el objeto de [**Directiva**](policy-object.md) local, como se muestra en [abrir un identificador de objeto de directiva](opening-a-policy-object-handle.md).

En el siguiente ejemplo se busca el SID de una cuenta, dado el nombre de cuenta.


```C++
void GetSIDInformation (LPWSTR AccountName,LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucName;
  PLSA_TRANSLATED_SID ltsTranslatedSID;
  PLSA_REFERENCED_DOMAIN_LIST lrdlDomainList;
  LSA_TRUST_INFORMATION myDomain;
  NTSTATUS ntsResult;
  PWCHAR DomainString = NULL;

  // Initialize an LSA_UNICODE_STRING with the name.
  if (!InitLsaString(&lucName, AccountName))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaLookupNames(
     PolicyHandle,     // handle to a Policy object
     1,                // number of names to look up
     &lucName,         // pointer to an array of names
     &lrdlDomainList,  // receives domain information
     &ltsTranslatedSID // receives relative SIDs
  );
  if (STATUS_SUCCESS != ntsResult) 
  {
    wprintf(L"Failed LsaLookupNames - %lu \n",
      LsaNtStatusToWinError(ntsResult));
    return;
  }

  // Get the domain the account resides in.
  myDomain = lrdlDomainList->Domains[ltsTranslatedSID->DomainIndex];
  DomainString = (PWCHAR) LocalAlloc(LPTR, myDomain.Name.Length + 1);
  wcsncpy_s(DomainString,
     myDomain.Name.Length + 1, 
     myDomain.Name.Buffer, 
     myDomain.Name.Length);

  // Display the relative Id. 
  wprintf(L"Relative Id is %lu in domain %ws.\n",
    ltsTranslatedSID->RelativeId,
    DomainString);

  LocalFree(DomainString);
  LsaFreeMemory(ltsTranslatedSID);
  LsaFreeMemory(lrdlDomainList);
}
```



En el ejemplo anterior, la función **InitLsaString** convierte una cadena Unicode en una estructura [**de \_ \_ cadena Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . El código de esta función se muestra en [mediante cadenas de Unicode LSA](using-lsa-unicode-strings.md).

> [!Note]  
> Estas funciones de traducción se proporcionan principalmente para que las usen los editores de permisos para mostrar información de la [*lista de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL). Un editor de permisos siempre debe llamar a estas funciones mediante el objeto de [**Directiva**](policy-object.md) del sistema en el que se encuentra el SID del [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) o el nombre. Esto garantiza que se haga referencia al conjunto adecuado de dominios de confianza durante la traducción.

 

Windows Access Control también proporciona funciones que realizan traducciones entre Sid y nombres de cuenta: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) y [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida). Si su aplicación necesita buscar un nombre de cuenta o SID y no usa la funcionalidad de directiva LSA adicional, utilice las funciones de Access Control de Windows en lugar de las funciones de directiva de LSA. Para obtener más información sobre estas funciones, vea [Access Control](/windows/desktop/SecAuthZ/access-control).

 

 
