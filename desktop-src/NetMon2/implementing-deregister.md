---
description: Monitor de red pasa todos los fotogramas de una captura a los analizadores y, a continuación, comienza a llamar a la función Deregister para todos los protocolos que identifica. Cada ARCHIVO DLL del analizador debe implementar una función Deregister para cada protocolo que admita el archivo DLL del analizador.
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: Implementación de Anulación del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee07c5b6b3c746e9c29811332b9e7674e49db26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069336"
---
# <a name="implementing-deregister"></a>Implementación de Anulación del registro

Monitor de red pasa todos los fotogramas de una captura a los analizadores y, a continuación, comienza a llamar a la función [**Deregister**](deregister.md) para todos los protocolos que identifica. Cada ARCHIVO DLL del analizador debe implementar una **función Deregister** para cada protocolo que admita el archivo DLL del analizador.

Cada implementación de la [**función Deregister**](deregister.md) debe llamar a la [**función DestroyProtocolDatabase**](destroypropertydatabase.md) para liberar los recursos que se usan para crear la base de datos.

El procedimiento siguiente identifica el paso necesario para implementar [**Deregister**](deregister.md).

**Para implementar Deregister para un protocolo**

-   Llame [**a DestroyProtocolDatabase para**](destroypropertydatabase.md) liberar los recursos de base de datos.

A continuación se muestra una implementación básica [**de Deregister**](deregister.md). Tenga en cuenta que el ejemplo de código muestra la versión de los recursos que se usan para crear una base de datos de propiedades.

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



