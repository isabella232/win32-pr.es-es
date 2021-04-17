---
description: Un objeto de evento es un objeto de sincronización cuyo estado se puede establecer explícitamente en señalado por el uso de la función SetEvent. A continuación se muestran los dos tipos de objeto de evento.
ms.assetid: 63dc2991-e070-4981-9e2d-90b4fdaaee7a
title: Objetos de eventos (sincronización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365b42bb7550507fe3522f07d950dac74c88843d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667979"
---
# <a name="event-objects-synchronization"></a>Objetos de eventos (sincronización)

Un *objeto de evento* es un objeto de sincronización cuyo estado se puede establecer explícitamente en señalado por el uso de la función [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) . A continuación se muestran los dos tipos de objeto de evento.



| Object             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento de restablecimiento manual | Objeto de evento cuyo estado permanece señalado hasta que se restablece explícitamente a no señalado por la función [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) . Mientras se señala, se puede liberar cualquier número de subprocesos en espera, o subprocesos que especifiquen posteriormente el mismo objeto de evento en una de las [funciones de espera](wait-functions.md).                                                                                                        |
| Evento de restablecimiento automático   | Objeto de evento cuyo estado permanece señalado hasta que se libera un único subproceso en espera, momento en el que el sistema establece automáticamente el estado en no señalado. Si no hay subprocesos en espera, el objeto del evento sigue teniendo el estado señalizado. Si hay más de un subproceso en espera, se selecciona un subproceso en espera. No asuma un orden FIFO (primero en salir, primero en salir). Los eventos externos como APC en modo kernel pueden cambiar el orden de espera.<br/> |



 

El objeto de evento es útil para enviar una señal a un subproceso que indica que se ha producido un evento determinado. Por ejemplo, en la entrada y la salida superpuestas, el sistema establece un objeto de evento especificado en el estado señalado cuando se ha completado la operación superpuesta. Un único subproceso puede especificar objetos de evento diferentes en varias operaciones simultáneas superpuestas y, a continuación, utilizar una de las [funciones de espera](wait-functions.md) de varios objetos para esperar a que se señale el estado de cualquiera de los objetos de evento.

Un subproceso utiliza la función [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) o [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) para crear un objeto de evento. El subproceso de creación especifica el estado inicial del objeto y si es un objeto de evento de restablecimiento manual o de restablecimiento automático. El subproceso de creación también puede especificar un nombre para el objeto de evento. Los subprocesos de otros procesos pueden abrir un identificador de un objeto de evento existente especificando su nombre en una llamada a la función [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa) . Para obtener más información sobre los nombres de los objetos mutex, Event, Semaphore y Timer, consulte [sincronización entre procesos](interprocess-synchronization.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar objetos de eventos](using-event-objects.md)
</dt> </dl>

 

 
