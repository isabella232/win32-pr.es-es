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
# <a name="opening-a-policy-object-handle"></a>Apertura de un identificador de objeto de Directiva

La mayoría de las funciones de directiva de LSA requieren un identificador para el objeto de [**Directiva**](policy-object.md) que el sistema debe consultar o modificar. Para obtener un identificador de un objeto de **Directiva** , llame a [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) y especifique el nombre del sistema al que desea obtener acceso y el conjunto de permisos de acceso necesarios.

Los permisos de acceso necesarios para la aplicación dependen de las acciones que realiza. Para obtener más información sobre los permisos necesarios para cada función, vea la descripción de esa función en [las funciones de directiva de LSA](management-functions.md).

Si la llamada a [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) se realiza correctamente, devuelve un identificador al objeto de [**Directiva**](policy-object.md) para el sistema especificado. A continuación, la aplicación pasa este identificador en las siguientes llamadas de función de directiva de LSA. Cuando la aplicación ya no necesita el identificador, debe llamar a [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) para liberarlo.

En el ejemplo siguiente se muestra cómo abrir un identificador de objeto de [**Directiva**](policy-object.md) .


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



En el ejemplo anterior, la aplicación solicitó \_ todos \_ los [*privilegios*](/windows/desktop/SecGloss/p-gly)de acceso. Para obtener más información sobre los permisos que debe solicitar la aplicación al llamar a [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), consulte las descripciones de las funciones a las que la aplicación pasará el identificador del objeto de [**Directiva**](policy-object.md) .

Para abrir un identificador para el objeto de [**Directiva**](policy-object.md) de un dominio de confianza, llame a [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (para crear una nueva relación de confianza con un dominio) o llame a [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (para tener acceso a un dominio de confianza existente). Ambas funciones establecen un puntero a un identificador de [**LSA \_**](lsa-handle.md), que puede especificar en las siguientes llamadas de función de directiva de LSA. Al igual que con [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), la aplicación debe llamar a [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) cuando ya no necesita el identificador del objeto de **Directiva** del dominio de confianza.

 

 
