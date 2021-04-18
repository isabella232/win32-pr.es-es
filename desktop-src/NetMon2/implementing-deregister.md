---
description: Monitor de red pasa todos los marcos de una captura a los analizadores y, a continuación, comienza a llamar a la función de eliminación de registros para todos los protocolos que identifica. Cada DLL del analizador debe implementar una función de eliminación de registro para cada protocolo que admita el archivo DLL del analizador.
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: Implementación de unregister
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee07c5b6b3c746e9c29811332b9e7674e49db26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652404"
---
# <a name="implementing-deregister"></a>Implementación de unregister

Monitor de red pasa todos los marcos de una captura a los analizadores y, a continuación, comienza a llamar a la función de [**eliminación de registros**](deregister.md) para todos los protocolos que identifica. Cada DLL del analizador debe implementar una función de **eliminación de registro** para cada protocolo que admita el archivo DLL del analizador.

Cada implementación de la función de [**eliminación de registros**](deregister.md) debe llamar a la función [**DestroyProtocolDatabase**](destroypropertydatabase.md) para liberar los recursos que se usan para crear la base de datos.

En el procedimiento siguiente se identifica el paso necesario para implementar [**unregister**](deregister.md).

**Para implementar el anulación del registro para un protocolo**

-   Llame a [**DestroyProtocolDatabase**](destroypropertydatabase.md) para liberar los recursos de la base de datos.

La siguiente es una implementación básica de [**unregister**](deregister.md). Tenga en cuenta que en el ejemplo de código se muestra la liberación de los recursos que se usan para crear una base de datos de propiedades.

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



