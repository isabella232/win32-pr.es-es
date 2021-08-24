---
description: Monitor de red pasa todos los fotogramas de una captura a los analizadores y, a continuación, comienza a llamar a la función Deregister para todos los protocolos que identifica. Cada ARCHIVO DLL del analizador debe implementar una función Deregister para cada protocolo que admita el archivo DLL del analizador.
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: Implementación de Anulación del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444502ba3ab19921a6372d4cda872aed85e879cbbdadc2f0176a7187bfc24491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890485"
---
# <a name="implementing-deregister"></a>Implementación de Anulación del registro

Monitor de red pasa todos los fotogramas de una captura a los analizadores y, a continuación, comienza a llamar a la función [**Deregister**](deregister.md) para todos los protocolos que identifica. Cada ARCHIVO DLL del analizador debe implementar una **función Deregister** para cada protocolo que admita el archivo DLL del analizador.

Cada implementación de la [**función Deregister**](deregister.md) debe llamar a la [**función DestroyProtocolDatabase**](destroypropertydatabase.md) para liberar los recursos que se usan para crear la base de datos.

El procedimiento siguiente identifica el paso necesario para implementar [**Deregister**](deregister.md).

**Para implementar Deregister para un protocolo**

-   Llame [**a DestroyProtocolDatabase para**](destroypropertydatabase.md) liberar los recursos de la base de datos.

A continuación se muestra una implementación básica [**de Deregister**](deregister.md). Tenga en cuenta que el ejemplo de código muestra la versión de los recursos que se usan para crear una base de datos de propiedades.

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



