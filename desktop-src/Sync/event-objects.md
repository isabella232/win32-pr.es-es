---
description: Un objeto de evento es un objeto de sincronización cuyo estado se puede establecer explícitamente en señalado mediante el uso de la función SetEvent. A continuación se enumeran los dos tipos de objeto de evento.
ms.assetid: 63dc2991-e070-4981-9e2d-90b4fdaaee7a
title: Objetos de evento (sincronización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9ea7c77fd61723b6ab927616817a5de2c323bf800431547800e2a96f33deee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886318"
---
# <a name="event-objects-synchronization"></a>Objetos de evento (sincronización)

Un *objeto de evento* es un objeto de sincronización cuyo estado se puede establecer explícitamente en señalado mediante el uso de la función [**SetEvent.**](/windows/win32/api/synchapi/nf-synchapi-setevent) A continuación se enumeran los dos tipos de objeto de evento.



| Object             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento de restablecimiento manual | Objeto de evento cuyo estado permanece señalado hasta que la función ResetEvent lo restablece explícitamente a [**sin signo.**](/windows/win32/api/synchapi/nf-synchapi-resetevent) Mientras se señala, se puede liberar cualquier número de subprocesos en espera [](wait-functions.md)o subprocesos que especifiquen posteriormente el mismo objeto de evento en una de las funciones de espera.                                                                                                        |
| Evento de restablecimiento automático   | Objeto de evento cuyo estado permanece señalado hasta que se libera un único subproceso en espera, momento en el que el sistema establece automáticamente el estado en no firma. Si no hay subprocesos en espera, el objeto del evento sigue teniendo el estado señalizado. Si hay más de un subproceso en espera, se selecciona un subproceso en espera. No asuma un orden FIFO (primero en in, primero en salir). Los eventos externos, como las API en modo kernel, pueden cambiar el orden de espera.<br/> |



 

El objeto de evento es útil para enviar una señal a un subproceso que indica que se ha producido un evento determinado. Por ejemplo, en la entrada y salida superpuestas, el sistema establece un objeto de evento especificado en el estado señalado cuando se ha completado la operación superpuesta. Un único subproceso puede especificar objetos de evento diferentes en varias operaciones [](wait-functions.md) superpuestas simultáneas y, a continuación, usar una de las funciones de espera de varios objetos para esperar a que se señale el estado de cualquiera de los objetos de evento.

Un subproceso usa las [**funciones CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) [**o CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) para crear un objeto de evento. El subproceso de creación especifica el estado inicial del objeto y si es un objeto de evento de restablecimiento manual o de restablecimiento automático. El subproceso de creación también puede especificar un nombre para el objeto de evento. Los subprocesos de otros procesos pueden abrir un identificador para un objeto de evento existente especificando su nombre en una llamada a la [**función OpenEvent.**](/windows/win32/api/synchapi/nf-synchapi-openeventa) Para obtener información adicional sobre los nombres de los objetos mutex, event, semaphore y timer, vea [Sincronización entre procesos.](interprocess-synchronization.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar objetos de evento](using-event-objects.md)
</dt> </dl>

 

 
