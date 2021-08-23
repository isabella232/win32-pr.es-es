---
description: 'Más información sobre: Errores extensibles Storage engine'
title: Errores extensibles Storage motor de ejecución
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 0c0ee0a4423d5b37913bd7922af07a7b2196a30176b2a1adca37240e03a28594
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721465"
---
# <a name="extensible-storage-engine-errors"></a>Errores extensibles Storage motor de ejecución


_**Se aplica a:** Windows | Windows Servidor_

## <a name="extensible-storage-engine-errors"></a>Errores extensibles Storage motor de ejecución

Todos los errores posibles devueltos por la API extensible Storage Engine (ESE) se definen mediante [el tipo JET_ERR](./jet-err.md) datos. Para obtener una lista de las marcas de error definidas para esta API, vea Extensible Storage Engine Error Codes ( Códigos de error extensibles del [motor de aplicaciones).](./extensible-storage-engine-error-codes.md)

A lo largo de la documentación de la API de ESE, solo se documentan los errores más importantes. Estos errores suelen representar errores de uso de API o condiciones de error muy importantes. Tenga en cuenta que cualquiera de estas API de ESE también puede devolver otros errores que no están documentados para cada API. En estos casos, el autor de la llamada simplemente debe controlar el error como lo haría con cualquier otro error devuelto por la API. A continuación, se puede usar el valor de error específico para fines de diagnóstico, como el seguimiento.

En general, un valor mayor que cero debe interpretarse como una advertencia, un valor de cero debe interpretarse como correcto y un valor menor que cero debe interpretarse como un error. Ninguna aplicación debe confiar en ningún otro patrón de estos valores (por ejemplo, intervalos de valores).

Cuando ESE encuentra algunos de los errores más graves, crea una entrada del registro de eventos que contiene detalles sobre los errores. El nivel de registro se puede controlar mediante parámetros [del registro de eventos](./event-log-parameters.md).

Algunas aplicaciones requieren la capacidad de [devolver](./jet-err.md)JET_ERR como HSULT. En el siguiente ejemplo de C++ se muestra cómo realizar esa conversión:

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

Para obtener información sobre cómo configurar parámetros del sistema para el control de errores, vea [Parámetros de control de errores](./error-handling-parameters.md).

### <a name="see-also"></a>Consulte también

[Parámetros de control de errores](./error-handling-parameters.md)

[Códigos de error Storage motor extensibles](./extensible-storage-engine-error-codes.md)

[JET_ERR](./jet-err.md)
