---
description: Muchas aplicaciones dependen de la relación de sincronización entre los eventos multimedia (por ejemplo, los dígitos DTMF recibidos) para determinar la naturaleza de una operación solicitada.
ms.assetid: 8d25a31f-de40-4c74-b8e7-a81fbfd47db2
title: Temporizadores de eventos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a584518c9c33e8991bd2388f01cb863bab1c7a3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689649"
---
# <a name="media-event-timers"></a>Temporizadores de eventos multimedia

Muchas aplicaciones dependen de la relación de sincronización entre los eventos multimedia (por ejemplo, los dígitos DTMF recibidos) para determinar la naturaleza de una operación solicitada. Por ejemplo, en una aplicación de correo de voz, dos dígitos de DTMF "1" consecutivos pueden significar "hacer una copia de seguridad de dos segmentos" o "reproducir desde el principio del mensaje", dependiendo de cuánto tiempo transcurrido entre los dos dígitos. En un entorno cliente/servidor, si la detección de DTMF se realiza en un procesador independiente del que se está ejecutando la aplicación, la latencia en la red de área local hace que sea muy probable que la relación de sincronización entre eventos multimedia se sesgado, con el resultado de que estas diferencias basadas en el tiempo podrían perderse o ser poco confiables.

Para resolver este problema, se puede asignar una marca de tiempo a varios mensajes TAPI. Dado que es el control de tiempo relativo entre estos eventos que es importante, el "tiempo de reloj" del evento no es importante y el tiempo de subsegundo está implicado, estas marcas de tiempo usan el "tiempo de resolución de milisegundos desde que se inició Windows" devuelto por la función [**GetTickCount**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount) . Las aplicaciones deben tener en cuenta que este es el número de pasos en el servidor (o el equipo donde se está ejecutando el proveedor de servicios que administra directamente el hardware) y no es necesariamente el mismo equipo en el que se ejecuta la aplicación. por lo tanto, las marcas de tiempo de estos mensajes TAPI solo se pueden comparar entre sí, y no con el valor devuelto por **GetTickCount** en el procesador en el que se ejecuta la aplicación.

Los mensajes TAPI que pueden marcarse como marcas de tiempo son: [**line \_ GATHERDIGITS**](line-gatherdigits.md), [**line \_ Generate**](line-generate.md), [**line \_ MONITORDIGITS**](line-monitordigits.md), [**line \_ MONITORMEDIA**](line-monitormedia.md)y [**line \_ MONITORTONE**](line-monitortone.md). El recuento de pasos se inserta en *dwParam3* de estos mensajes. Si el proveedor de servicios no admite la marca de tiempo (que se indica mediante la configuración del proveedor de servicios *dwParam3* en estos mensajes en 0), TAPI insertará el número de pasos en *dwParam3* de todos estos mensajes (se puede sesgar en cierto modo, pero menor que si la aplicación hizo lo mismo después de que los mensajes hubieran recorrido un esquema de comunicación entre procesos).

 

 
