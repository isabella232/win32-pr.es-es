---
description: La mayoría de las funciones de directiva de LSA requieren un identificador para el objeto de directiva que el sistema debe consultar o modificar. Para obtener un identificador de un objeto de Directiva, llame a LsaOpenPolicy y especifique el nombre del sistema al que desea obtener acceso y el conjunto de permisos de acceso necesarios.
ms.assetid: 66fdc878-d9c4-421c-b79f-9df08984611c
title: Apertura de un identificador de objeto de Directiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c187720692db4937b6e1299dd2bb63fac647852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688534"
---
# <a name="opening-a-policy-object-handle"></a><span data-ttu-id="42364-104">Apertura de un identificador de objeto de Directiva</span><span class="sxs-lookup"><span data-stu-id="42364-104">Opening a Policy Object Handle</span></span>

<span data-ttu-id="42364-105">La mayoría de las funciones de directiva de LSA requieren un identificador para el objeto de [**Directiva**](policy-object.md) que el sistema debe consultar o modificar.</span><span class="sxs-lookup"><span data-stu-id="42364-105">Most LSA Policy functions require a handle to the [**Policy**](policy-object.md) object for the system to query or modify.</span></span> <span data-ttu-id="42364-106">Para obtener un identificador de un objeto de **Directiva** , llame a [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) y especifique el nombre del sistema al que desea obtener acceso y el conjunto de permisos de acceso necesarios.</span><span class="sxs-lookup"><span data-stu-id="42364-106">To obtain a handle to a **Policy** object, call [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) and specify the name of the system you want to access and the set of access permissions required.</span></span>

<span data-ttu-id="42364-107">Los permisos de acceso necesarios para la aplicación dependen de las acciones que realiza.</span><span class="sxs-lookup"><span data-stu-id="42364-107">The access permissions required for your application depend on the actions it performs.</span></span> <span data-ttu-id="42364-108">Para obtener más información sobre los permisos necesarios para cada función, vea la descripción de esa función en [las funciones de directiva de LSA](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="42364-108">For details about the permissions required for each function, see the description of that function in [LSA Policy Functions](management-functions.md).</span></span>

<span data-ttu-id="42364-109">Si la llamada a [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) se realiza correctamente, devuelve un identificador al objeto de [**Directiva**](policy-object.md) para el sistema especificado.</span><span class="sxs-lookup"><span data-stu-id="42364-109">If the call to [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) is successful, it returns a handle to the [**Policy**](policy-object.md) object for the specified system.</span></span> <span data-ttu-id="42364-110">A continuación, la aplicación pasa este identificador en las siguientes llamadas de función de directiva de LSA.</span><span class="sxs-lookup"><span data-stu-id="42364-110">Your application then passes this handle in subsequent LSA Policy function calls.</span></span> <span data-ttu-id="42364-111">Cuando la aplicación ya no necesita el identificador, debe llamar a [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) para liberarlo.</span><span class="sxs-lookup"><span data-stu-id="42364-111">When your application no longer needs the handle, it should call [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) to free it.</span></span>

<span data-ttu-id="42364-112">En el ejemplo siguiente se muestra cómo abrir un identificador de objeto de [**Directiva**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="42364-112">The following example shows how to open a [**Policy**](policy-object.md) object handle.</span></span>


```C++
#include <windows.h>

#define TARGET_SYSTEM_NAME L"mysystem"

LSA_HANDLE GetPolicyHandle()
{
  LSA_OBJECT_ATTRIBUTES ObjectAttributes;
  WCHAR SystemName[] = TARGET_SYSTEM_NAME;
  USHORT SystemNameLength;
  LSA_UNICODE_STRING lusSystemName;
  NTSTATUS ntsResult;
  LSA_HANDLE lsahPolicyHandle;

  // Object attributes are reserved, so initialize to zeros.
  ZeroMemory(&ObjectAttributes, sizeof(ObjectAttributes));

  //Initialize an LSA_UNICODE_STRING to the server name.
  SystemNameLength = wcslen(SystemName);
  lusSystemName.Buffer = SystemName;
  lusSystemName.Length = SystemNameLength * sizeof(WCHAR);
  lusSystemName.MaximumLength = (SystemNameLength+1) * sizeof(WCHAR);

  // Get a handle to the Policy object.
  ntsResult = LsaOpenPolicy(
        &lusSystemName,    //Name of the target system.
        &ObjectAttributes, //Object attributes.
        POLICY_ALL_ACCESS, //Desired access permissions.
        &lsahPolicyHandle  //Receives the policy handle.
    );

  if (ntsResult != STATUS_SUCCESS)
  {
    // An error occurred. Display it as a win32 error code.
    wprintf(L"OpenPolicy returned %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return NULL;
  } 
  return lsahPolicyHandle;
}
```



<span data-ttu-id="42364-113">En el ejemplo anterior, la aplicación solicitó \_ todos \_ los [*privilegios*](/windows/desktop/SecGloss/p-gly)de acceso.</span><span class="sxs-lookup"><span data-stu-id="42364-113">In the preceding example, the application requested POLICY\_ALL\_ACCESS [*privileges*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="42364-114">Para obtener más información sobre los permisos que debe solicitar la aplicación al llamar a [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), consulte las descripciones de las funciones a las que la aplicación pasará el identificador del objeto de [**Directiva**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="42364-114">For details about which permissions your application should request when calling [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), see the descriptions of the functions that your application will pass the [**Policy**](policy-object.md) object handle to.</span></span>

<span data-ttu-id="42364-115">Para abrir un identificador para el objeto de [**Directiva**](policy-object.md) de un dominio de confianza, llame a [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (para crear una nueva relación de confianza con un dominio) o llame a [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (para tener acceso a un dominio de confianza existente).</span><span class="sxs-lookup"><span data-stu-id="42364-115">To open a handle to the [**Policy**](policy-object.md) object of a trusted domain, call [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (to create a new trust relationship with a domain) or call [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (to access an existing trusted domain).</span></span> <span data-ttu-id="42364-116">Ambas funciones establecen un puntero a un identificador de [**LSA \_**](lsa-handle.md), que puede especificar en las siguientes llamadas de función de directiva de LSA.</span><span class="sxs-lookup"><span data-stu-id="42364-116">Both of these functions set a pointer to an [**LSA\_HANDLE**](lsa-handle.md), which you can then specify in subsequent LSA Policy function calls.</span></span> <span data-ttu-id="42364-117">Al igual que con [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), la aplicación debe llamar a [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) cuando ya no necesita el identificador del objeto de **Directiva** del dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="42364-117">As with [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), your application should call [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) when it no longer needs the handle to the trusted domain's **Policy** object.</span></span>

 

 
