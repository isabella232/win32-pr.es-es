---
title: Tiempo de espera de búsqueda
description: Un cliente también puede imponer un límite de tiempo que esperará a que un servidor devuelva el conjunto de resultados.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- ADSI de tiempo de espera de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfdc63dd4490a840a16eb61598b2461c3e1a40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356693"
---
# <a name="search-time-out"></a>Tiempo de espera de búsqueda

Un cliente también puede imponer un límite de tiempo que esperará a que un servidor devuelva el conjunto de resultados. El valor de la opción "tiempo de espera de la búsqueda" especifica este límite. Cuando el servidor no responde a una consulta dentro del período de tiempo especificado, el cliente puede detener la búsqueda e intentarlo de nuevo más tarde.

La propiedad de tiempo de espera resulta útil cuando un cliente solicita una búsqueda asincrónica. En una búsqueda asincrónica, el cliente realiza una solicitud y, a continuación, continúa con otras tareas mientras espera a que el servidor devuelva los resultados. Es posible que el servidor se quede sin conexión sin notificar al cliente. En este caso, el cliente no tiene forma de reconocer que el servidor sigue procesando la consulta o si ha dejado de estar activa. La propiedad de tiempo de espera proporciona al cliente algún control de estos casos.

Para obtener más información acerca del uso de la opción de tiempo de espera de búsqueda con una interfaz de búsqueda específica, vea:

-   [Límite de tiempo de cliente con IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Buscar con Objetos de datos ActiveX](searching-with-activex-data-objects-ado.md)
-   [Buscar con OLE DB](searching-with-ole-db.md)

 

 




