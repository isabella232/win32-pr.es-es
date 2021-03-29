---
title: Montón
description: Un montón realiza un seguimiento de un grupo de asignaciones que se liberan como una unidad.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Servicios Web de montón para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e1651f90b8ad1afca8f85f9dd2e6f10fc7f5c3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421656"
---
# <a name="heap"></a>Montón

Un montón realiza un seguimiento de un grupo de asignaciones que se liberan como una unidad.

Esto le permite evitar patrones complejos de asignación y desasignación de memoria cuando se usa WWSAPI.


Hay un montón asociado a cada mensaje. A medida que se envía un mensaje, o cuando se recibe un mensaje, se usa el montón del mensaje para cualquier asignación relacionada con ese mensaje concreto. Una vez que se envía o recibe un mensaje, se restablece el montón (que limpia las asignaciones relacionadas con el mensaje determinado).

Los montones también se pueden usar para almacenar datos de mensajes de forma independiente de la duración de un mensaje. Muchas de las especificaciones de permiso de la API del montón que se van a usar al leer los datos proporcionan un control explícito sobre la duración de cualquier lectura de datos.

Se garantiza que las asignaciones de un montón estén alineadas en al menos un límite de 8 bytes.

Las asignaciones de cero bytes devolverán un puntero no nulo.

En Windows 7, si PageHeap está habilitada, se usa un montón devuelto de HeapCreate para administrar la memoria. En este caso, [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) se asigna directamente a HeapAlloc y [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) a HeapDestroy.

La siguiente enumeración se usa con el montón:

-   [**identificador de la \_ propiedad del montón WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

Las siguientes funciones se usan con el montón:

-   [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [**WsCreateHeap**](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [**WsFreeHeap**](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [**WsGetHeapProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

El siguiente identificador se usa con el montón:

-   [\_montón WS](ws-heap.md)

Las siguientes estructuras se usan con el montón:

-   [**\_propiedades del montón WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [**\_propiedad del montón WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




