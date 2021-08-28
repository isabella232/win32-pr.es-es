---
title: Montón
description: Un montón realiza un seguimiento de un grupo de asignaciones que se liberan como una unidad.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Servicios web de montón para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a581d4173ed16423ac55e82d3dde356bad1e310047dd44d8f92fded0c6f458e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005935"
---
# <a name="heap"></a>Montón

Un montón realiza un seguimiento de un grupo de asignaciones que se liberan como una unidad.

Esto le permite evitar patrones complejos de asignación y desasignación de memoria cuando se usa WWSAPI.


Hay un montón asociado a cada mensaje. A medida que se envía un mensaje o cuando se recibe un mensaje, el montón del mensaje se usa para las asignaciones relacionadas con ese mensaje concreto. Después de enviar o recibir un mensaje, se restablece el montón (que limpia las asignaciones relacionadas con el mensaje determinado).

Los montones también se pueden usar para almacenar los datos del mensaje por separado de la duración de un mensaje. Muchas de las especificaciones de permiso de la API del montón que se usan al leer datos dan un control explícito sobre la duración de cualquier lectura de datos.

Se garantiza que las asignaciones de un montón se alinean en al menos un límite de 8 bytes.

Las asignaciones de cero bytes devolverán un puntero que no es NULL.

En Windows 7, si PageHeap está habilitado, se usa un montón devuelto desde HeapCreate para administrar la memoria. En este caso, [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) se asigna directamente a HeapAlloc y [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) se asigna a HeapDestroy.

La enumeración siguiente se usa con el montón:

-   [**IDENTIFICADOR DE PROPIEDAD \_ DEL MONTÓN \_ DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

Las siguientes funciones se usan con el montón:

-   [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [**WsCreateHeap**](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [**WsFreeHeap**](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [**WsGetHeapProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

El siguiente identificador se usa con el montón:

-   [MONTÓN \_ de WS](ws-heap.md)

Las estructuras siguientes se usan con el montón:

-   [**PROPIEDADES DEL MONTÓN DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [**WS \_ HEAP \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




