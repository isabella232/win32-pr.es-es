---
description: La Directiva de LSA proporciona dos funciones que puede usar para establecer y recuperar datos privados.
ms.assetid: 7b6e63d4-ce8f-4279-85d9-da6b2b589afa
title: Almacenar datos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6281f77e66a4217bda534b34342d6cefd92bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423767"
---
# <a name="storing-private-data"></a>Almacenar datos privados

La Directiva de LSA proporciona dos funciones que puede usar para establecer y recuperar datos privados. Estos datos se almacenan como una cadena cifrada en el registro. Por ejemplo, puede utilizar estas funciones para almacenar contraseñas de cuentas de servidor y otra información confidencial.

Llame a la función [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) para almacenar y cifrar los datos privados. Como se describe en [Private Data Object](private-data-object.md), los objetos de datos privados incluyen tres tipos especializados: local, global y Machine. Para crear un objeto especializado, agregue un prefijo al nombre de clave que se pasa a **LsaStorePrivateData**: "L $" para los objetos locales, "G $" para los objetos globales y "M $" para los objetos de equipo. Si no va a crear uno de estos tipos especializados, no es necesario especificar un prefijo de nombre de clave.

Para recuperar y descodificar los datos privados almacenados previamente, llame a [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata). Tenga en cuenta que no puede recuperar objetos de datos privados del equipo; los objetos de equipo solo se pueden recuperar mediante el sistema operativo.

Antes de poder almacenar o recuperar datos privados, la aplicación debe obtener un identificador para el objeto de [**Directiva**](policy-object.md) local, como se muestra en [abrir un identificador de objeto de directiva](opening-a-policy-object-handle.md).

En el ejemplo siguiente se crea un objeto de datos privado local. Tenga en cuenta que la función InitLsaString convierte una cadena [*Unicode*](/windows/desktop/SecGloss/u-gly) en una estructura de [**\_ \_ cadena Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . El código de esta función se muestra en [mediante cadenas de Unicode LSA](using-lsa-unicode-strings.md).


```C++
#include <windows.h>
#include <stdio.h>

BOOL CreatePrivateDataObject(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult;
  LSA_UNICODE_STRING lucKeyName;
  LSA_UNICODE_STRING lucPrivateData;
  // The L$ prefix specifies a local private data object
  WCHAR wszKeyName[] = L"L$MyPrivateKey";
  WCHAR wszPrivateData[] = L"Something secret.";

  // Initializing PLSA_UNICODE_STRING structures
  if (!InitLsaString(&lucKeyName, wszKeyName))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }
  if (!InitLsaString(&lucPrivateData, wszPrivateData))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }

  // Store the private data.
  ntsResult = LsaStorePrivateData(
    PolicyHandle,   // handle to a Policy object
    &lucKeyName,    // key to identify the data
    &lucPrivateData // the private data
  );
  if (ntsResult != STATUS_SUCCESS)
  {
    wprintf(L"Store private object failed %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return FALSE;
  }
  return TRUE;
}
```



> [!Note]  
> Los datos almacenados por la función [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) no están totalmente protegidos. La clave, sin embargo, tiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) que permite que solo el creador y los administradores lean los datos.

 

 

 
