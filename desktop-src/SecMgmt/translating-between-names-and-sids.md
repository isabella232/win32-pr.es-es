---
description: La autoridad de seguridad local (LSA) proporciona funciones para traducir entre los nombres de usuario, grupo y grupo local y sus valores de identificador de seguridad (SID) correspondientes.
ms.assetid: 8845b709-a8f9-4d0f-a4a6-86d23d6b01d5
title: Traducción entre nombres y SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417034a99331c09f20546f2f352bc762a86f02e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069005"
---
# <a name="translating-between-names-and-sids"></a>Traducción entre nombres y SID

La [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) proporciona funciones para traducir entre los nombres de usuario, grupo y grupo local y sus valores de identificador de seguridad (SID) correspondientes. [](/windows/desktop/SecGloss/s-gly) Para buscar nombres de cuenta, llame a la [**función LsaLookupNames.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) Esta función devuelve el SID como un par de índice rid/dominio. Para obtener el SID como un único elemento, llame a la función [**LsaLookupNames2.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) Para buscar SID, llame a [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).

Estas funciones pueden traducir la información de nombre y SID de cualquier dominio de confianza para el sistema local.

Para poder traducir entre nombres de cuenta y SID, la aplicación debe obtener un identificador para el objeto [**de**](policy-object.md) directiva local, como se muestra en Apertura de un identificador de [objeto de directiva](opening-a-policy-object-handle.md).

En el ejemplo siguiente se busca el SID de una cuenta, dado el nombre de la cuenta.


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



En el ejemplo anterior, la función **InitLsaString** convierte una cadena Unicode en una estructura [**\_ STRING UNICODE \_ LSA.**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) El código de esta función se muestra en [Using LSA Unicode Strings](using-lsa-unicode-strings.md).

> [!Note]  
> Estas funciones de traducción se proporcionan principalmente para que las usen los editores de permisos para mostrar información de la lista de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACL). Un editor de permisos siempre debe llamar a estas funciones mediante el [**objeto Policy**](policy-object.md) del sistema en el que se encuentra el [*NOMBRE*](/windows/desktop/SecGloss/s-gly) o el IDENTIFICADOR de seguridad SID. Esto garantiza que se haga referencia al conjunto adecuado de dominios de confianza durante la traducción.

 

Windows Access Control también proporciona funciones que realizan traducciones entre SID y nombres de cuenta: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) y [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida). Si la aplicación necesita buscar un nombre de cuenta o SID y no usa la funcionalidad de directiva de LSA adicional, use las funciones Windows Access Control en lugar de las funciones de directiva LSA. Para obtener más información sobre estas funciones, [vea Access Control](/windows/desktop/SecAuthZ/access-control).

 

 
