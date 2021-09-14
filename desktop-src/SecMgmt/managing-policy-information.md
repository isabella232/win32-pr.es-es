---
description: El LSA proporciona funciones que los administradores pueden usar para consultar y establecer información de directiva global para el equipo local y el dominio.
ms.assetid: bbe27d16-0a6b-435a-ae80-5e983047b511
title: Administración de la información de directiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc76137f41c592370dbeecafd243f11012cb1e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073605"
---
# <a name="managing-policy-information"></a>Administración de la información de directiva

El LSA proporciona funciones que los administradores pueden usar para consultar y establecer información de directiva global para el equipo local y el dominio.

Para poder administrar la información de la directiva, la aplicación debe obtener un identificador para el objeto [**de**](policy-object.md) directiva local, como se muestra en Apertura de un [identificador de objeto de directiva](opening-a-policy-object-handle.md). Este identificador lo requieren las funciones que administran la información de la directiva.

Para recuperar información sobre la directiva de seguridad local, llame a [**LsaQueryInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy). Para establecer la directiva de seguridad local, llame [**a LsaSetInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy). La descripción de la [**enumeración POLICY \_ INFORMATION \_ CLASS**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class) detalla los tipos de información de directiva que se pueden consultar o establecer.

En el ejemplo siguiente se muestra cómo obtener información de dominio de cuenta de un sistema, dado un identificador al objeto [**Policy del**](policy-object.md) sistema.


```C++
#include <windows.h>

BOOL GetAccountDomainInfo(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult = STATUS_SUCCESS;
  PPOLICY_ACCOUNT_DOMAIN_INFO pPADInfo = NULL;
  PWCHAR name = NULL;
  UINT nameSize;
  
  ntsResult = LsaQueryInformationPolicy(
    PolicyHandle,                   // Open handle to a Policy object.
    PolicyAccountDomainInformation, // The information to get.
    (PVOID *)&pPADInfo              // Storage for the information.
  );

  if (ntsResult == STATUS_SUCCESS)
  {  
    // There is no guarantee that the LSA_UNICODE_STRING buffer
    // is null-terminated, so copy the name to a buffer that is.
    nameSize =  pPADInfo->DomainName.Length + 1 * sizeof(WCHAR);
    name = (WCHAR *) LocalAlloc(LPTR, nameSize);
    if (!name)
    {
        wprintf(L"Failed LocalAlloc\n");
        exit(1);
    }
    wcsncpy_s(name, nameSize, pPADInfo->DomainName.Buffer,
        pPADInfo->DomainName.Length);
    wprintf(L"The account domain name is %ws\n", name);
    LocalFree(name);
    if (STATUS_SUCCESS != LsaFreeMemory(pPADInfo))
        wprintf(L"LsaFreeMemory error\n");
  }
  else
  {
    // Show the corresponding win32 error code.
    wprintf(
        L"Error obtaining account domain information - (win32) %lu\n",
        LsaNtStatusToWinError(ntsResult));
  }

  return !ntsResult;
}

```



 

 
