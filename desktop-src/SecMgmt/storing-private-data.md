---
description: La directiva LSA proporciona dos funciones que puede usar para establecer y recuperar datos privados.
ms.assetid: 7b6e63d4-ce8f-4279-85d9-da6b2b589afa
title: Almacenamiento de datos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6281f77e66a4217bda534b34342d6cefd92bd7d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069020"
---
# <a name="storing-private-data"></a>Almacenamiento de datos privados

La directiva LSA proporciona dos funciones que puede usar para establecer y recuperar datos privados. Estos datos se almacenan como una cadena cifrada en el Registro. Por ejemplo, puede usar estas funciones para almacenar contraseñas de cuenta de servidor y otra información confidencial.

Llame a [**la función LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) para almacenar y cifrar datos privados. Como se describe en [Private Data Object ,](private-data-object.md)los objetos de datos privados incluyen tres tipos especializados: local, global y máquina. Para crear un objeto especializado, agregue un prefijo al nombre de clave pasado a **LsaStorePrivateData:**"L$" para objetos locales, "G$" para objetos globales y "M$" para objetos de máquina. Si no va a crear uno de estos tipos especializados, no es necesario especificar un prefijo de nombre de clave.

Para recuperar y descodificar datos privados previamente almacenados, llame a [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata). Tenga en cuenta que no puede recuperar objetos de datos privados de la máquina; Los objetos de máquina solo los puede recuperar el sistema operativo.

Para poder almacenar o recuperar datos privados, la aplicación debe obtener un identificador para el objeto [**Policy**](policy-object.md) local, como se muestra en Apertura de un identificador de [objeto de directiva](opening-a-policy-object-handle.md).

En el ejemplo siguiente se crea un objeto de datos privado local. Tenga en cuenta que la función InitLsaString convierte una [*cadena Unicode*](/windows/desktop/SecGloss/u-gly) en una estructura STRING [**UNICODE \_ \_ LSA.**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) El código de esta función se muestra en [Using LSA Unicode Strings (Uso de cadenas Unicode LSA).](using-lsa-unicode-strings.md)


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
> Los datos almacenados por [**la función LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) no están absolutamente protegidos. Sin embargo, la clave tiene una [*lista de control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) que permite que solo el creador y los administradores lean los datos.

 

 

 
