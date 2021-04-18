---
description: LSA proporciona funciones que los administradores pueden usar para consultar y establecer información global de directivas para el equipo local y el dominio.
ms.assetid: bbe27d16-0a6b-435a-ae80-5e983047b511
title: Administrar la información de directivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc76137f41c592370dbeecafd243f11012cb1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668318"
---
# <a name="managing-policy-information"></a><span data-ttu-id="bcde8-103">Administrar la información de directivas</span><span class="sxs-lookup"><span data-stu-id="bcde8-103">Managing Policy Information</span></span>

<span data-ttu-id="bcde8-104">LSA proporciona funciones que los administradores pueden usar para consultar y establecer información global de directivas para el equipo local y el dominio.</span><span class="sxs-lookup"><span data-stu-id="bcde8-104">The LSA provides functions that administrators can use to query and set global policy information for the local computer and the domain.</span></span>

<span data-ttu-id="bcde8-105">Antes de poder administrar la información de directivas, la aplicación debe obtener un identificador para el objeto de [**Directiva**](policy-object.md) local, como se muestra en [abrir un identificador de objeto de directiva](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="bcde8-105">Before you can manage policy information, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span> <span data-ttu-id="bcde8-106">Este identificador es necesario para las funciones que administran la información de directivas.</span><span class="sxs-lookup"><span data-stu-id="bcde8-106">This handle is required by the functions that manage policy information.</span></span>

<span data-ttu-id="bcde8-107">Para recuperar información acerca de la Directiva de seguridad local, llame a [**LsaQueryInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy).</span><span class="sxs-lookup"><span data-stu-id="bcde8-107">To retrieve information about the local security policy, call [**LsaQueryInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy).</span></span> <span data-ttu-id="bcde8-108">Para establecer la Directiva de seguridad local, llame a [**LsaSetInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy).</span><span class="sxs-lookup"><span data-stu-id="bcde8-108">To set local security policy, call [**LsaSetInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy).</span></span> <span data-ttu-id="bcde8-109">La descripción de la enumeración de la [**\_ \_ clase de información de directiva**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class) detalla los tipos de información de directivas que se pueden consultar o establecer.</span><span class="sxs-lookup"><span data-stu-id="bcde8-109">The description of the [**POLICY\_INFORMATION\_CLASS**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class) enumeration details the types of policy information that can be queried or set.</span></span>

<span data-ttu-id="bcde8-110">En el ejemplo siguiente se muestra cómo obtener la información de dominio de la cuenta de un sistema, dado un identificador para el objeto de [**Directiva**](policy-object.md) del sistema.</span><span class="sxs-lookup"><span data-stu-id="bcde8-110">The following example demonstrates how to obtain a system's account domain information, given a handle to the system's [**Policy**](policy-object.md) object.</span></span>


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



 

 
