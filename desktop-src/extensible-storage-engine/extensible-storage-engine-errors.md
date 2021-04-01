---
description: Más información acerca de los errores del motor de almacenamiento extensible
title: Errores del motor de almacenamiento extensible
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 55c86d51f44414688897d6450adf214a0478f7d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913585"
---
# <a name="extensible-storage-engine-errors"></a>Errores del motor de almacenamiento extensible


_**Se aplica a:** Windows | Windows Server_

## <a name="extensible-storage-engine-errors"></a>Errores del motor de almacenamiento extensible

Todos los errores posibles devueltos por la API del motor de almacenamiento extensible (ESE) se definen mediante el tipo de datos [JET_ERR](./jet-err.md) . Para obtener una lista de las marcas de error definidas para esta API, vea [códigos de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md).

En la documentación de la API de ESE, solo se documentan los errores más importantes. Estos errores suelen representar errores de uso de la API o condiciones de error muy importantes. Tenga en cuenta que cualquiera de estas API de ESE también puede devolver otros errores que no están documentados para cada API. En estos casos, el autor de la llamada simplemente debe controlar el error como cualquier otro error devuelto por la API. El valor de error específico se puede usar para fines de diagnóstico como el seguimiento.

En general, un valor mayor que cero debe interpretarse como una advertencia, el valor cero debe interpretarse como correcto y un valor menor que cero debe interpretarse como un error. No es necesario que una aplicación confíe en otros patrones de estos valores (por ejemplo, intervalos de valores).

Cuando ESE encuentra algunos de los errores más graves, crea una entrada en el registro de eventos que contiene detalles sobre los errores. El nivel de registro se puede controlar mediante [parámetros del registro de eventos](./event-log-parameters.md).

Algunas aplicaciones requieren la capacidad de devolver [JET_ERR](./jet-err.md)s como valores HRESULT. En el siguiente ejemplo de C++ se muestra cómo hacer esa conversión:

```cpp
    #ifndef FACILITY_JET_ERR
    #define FACILITY_JET_ERR 0xE5E
    #endif
    #ifndef HRESULT_FROM_JET_ERR
    #define HRESULT_FROM_JET_ERR( __err )
    (
      ( __err ) == JET_errSuccess ?
      S_OK :
      (
        ( __err ) == JET_errOutOfMemory ?
        E_OUTOFMEMORY :
        MAKE_HRESULT
        (
          (
            ( __err ) < 0 ?
            SEVERITY_ERROR :
            SEVERITY_SUCCESS
          ),
          FACILITY_JET_ERR,
          (
            ( __err ) < 0 ?
            -( __err ) :
            ( __err )
          )
          & 0xFFFF
        )
      )
    )
    
    #endif
```

Para obtener información sobre cómo configurar los parámetros del sistema para el control de errores, consulte [parámetros de control de errores](./error-handling-parameters.md).

### <a name="see-also"></a>Consulte también

[Parámetros de control de errores](./error-handling-parameters.md)

[Códigos de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md)

[JET_ERR](./jet-err.md)
