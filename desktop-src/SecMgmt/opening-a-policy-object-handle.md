---
description: La mayoría de las funciones de directiva LSA requieren un identificador para el objeto Policy para que el sistema consulte o modifique. Para obtener un identificador para un objeto Policy, llame a LsaOpenPolicy y especifique el nombre del sistema al que desea acceder y el conjunto de permisos de acceso necesarios.
ms.assetid: 66fdc878-d9c4-421c-b79f-9df08984611c
title: Apertura de un identificador de objeto de directiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c187720692db4937b6e1299dd2bb63fac647852
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073598"
---
# <a name="opening-a-policy-object-handle"></a>Apertura de un identificador de objeto de directiva

La mayoría de las funciones de directiva LSA requieren un identificador para el [**objeto Policy**](policy-object.md) para que el sistema consulte o modifique. Para obtener un identificador para un objeto **Policy,** llame a [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) y especifique el nombre del sistema al que desea acceder y el conjunto de permisos de acceso necesarios.

Los permisos de acceso necesarios para la aplicación dependen de las acciones que realiza. Para obtener más información sobre los permisos necesarios para cada función, vea la descripción de esa función en [Funciones de directiva de LSA](management-functions.md).

Si la llamada a [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) se realiza correctamente, devuelve un identificador al [**objeto Policy**](policy-object.md) para el sistema especificado. A continuación, la aplicación pasa este identificador en posteriores llamadas a funciones de la directiva LSA. Cuando la aplicación ya no necesite el identificador, debe llamar a [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) para liberarlo.

En el ejemplo siguiente se muestra cómo abrir un [**identificador de objeto**](policy-object.md) policy.


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



En el ejemplo anterior, la aplicación solicitó los \_ \_ [*privilegios*](/windows/desktop/SecGloss/p-gly)POLICY ALL ACCESS . Para obtener más información sobre qué permisos debe solicitar la aplicación al llamar a [**LsaOpenPolicy,**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)vea las descripciones de las funciones a las que la aplicación pasará el identificador de [**objeto**](policy-object.md) Policy.

Para abrir un identificador para el objeto [**Policy**](policy-object.md) de un dominio de confianza, llame a [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (para crear una nueva relación de confianza con un dominio) o llame a [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (para acceder a un dominio de confianza existente). Ambas funciones establecen un puntero a [**un identificador de LSA, \_**](lsa-handle.md)que puede especificar en las llamadas a funciones de la directiva LSA subsiguientes. Al igual [**que con LsaOpenPolicy,**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)la aplicación debe llamar a [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) cuando ya no necesite el identificador del objeto Policy del **dominio de** confianza.

 

 
