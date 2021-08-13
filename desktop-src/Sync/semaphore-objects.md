---
description: Un objeto semáforo es un objeto de sincronización que mantiene un recuento entre cero y un valor máximo especificado.
ms.assetid: d9da1d98-a306-4e2d-a149-1eef6a724751
title: Objetos semáforos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c814be0ab2fafe7fbabfdeca5b640cfb550172a09e465dddc71629dfa5b0068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886264"
---
# <a name="semaphore-objects"></a>Objetos semáforos

Un *objeto semáforo* es un objeto de sincronización que mantiene un recuento entre cero y un valor máximo especificado. El recuento se disminuye cada vez que un subproceso completa una espera para el objeto de semáforo y se incrementa cada vez que un subproceso libera el semáforo. Cuando el recuento alcanza cero, ningún subproceso puede esperar correctamente a que se señale el estado del objeto de semáforo. El estado de un semáforo se establece como señalizado cuando su recuento es mayor que cero y como no señalizado cuando su recuento es cero.

El objeto semáforo es útil para controlar un recurso compartido que puede admitir un número limitado de usuarios. Actúa como una puerta que limita el número de subprocesos que comparten el recurso a un número máximo especificado. Por ejemplo, una aplicación podría colocar un límite en el número de ventanas que crea. Usa un semáforo con un recuento máximo igual al límite de ventana, lo que disminuye el recuento cada vez que se crea una ventana e incrementa cada vez que se cierra una ventana. La aplicación especifica el objeto semáforo en la llamada a una de las funciones [de espera](wait-functions.md) antes de crear cada ventana. Cuando el recuento es cero, lo que indica que se ha alcanzado el límite de ventana, la función wait bloquea la ejecución del código de creación de ventana.

Un subproceso usa las [**funciones CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea) o [**CreateSemaphoreEx**](/windows/desktop/api/WinBase/nf-winbase-createsemaphoreexa) para crear un objeto semáforo. El subproceso de creación especifica el recuento inicial y el valor máximo del recuento para el objeto . El recuento inicial no debe ser menor que cero ni mayor que el valor máximo. El subproceso de creación también puede especificar un nombre para el objeto semáforo. Los subprocesos de otros procesos pueden abrir un identificador para un objeto de semáforo existente especificando su nombre en una llamada a la [**función OpenSemaphore.**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew) Para obtener información adicional sobre los nombres de los objetos mutex, event, semaphore y timer, vea [Sincronización entre procesos.](interprocess-synchronization.md)

Si hay más de un subproceso esperando en un semáforo, se selecciona un subproceso en espera. No asuma un orden FIFO (primero en in, primero en salir). Los eventos externos, como las API en modo kernel, pueden cambiar el orden de espera.

Cada vez que [](wait-functions.md) se devuelve una de las funciones de espera porque el estado de un semáforo se estableció en señalado, el recuento del semáforo se reduce en uno. La [**función ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) aumenta el recuento de un semáforo en una cantidad especificada. El recuento nunca puede ser menor que cero o mayor que el valor máximo.

El recuento inicial de un semáforo normalmente se establece en el valor máximo. A continuación, el recuento se disminuye de ese nivel a medida que se consume el recurso protegido. Como alternativa, puede crear un semáforo con un recuento inicial de cero para bloquear el acceso al recurso protegido mientras se inicializa la aplicación. Después de la inicialización, puede usar [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) para incrementar el recuento al valor máximo.

Un subproceso que posee un objeto de exclusión mutua puede esperar repetidamente a que el mismo objeto de exclusión mutua se señale sin que su ejecución se bloquee. Sin embargo, un subproceso que espera repetidamente el mismo objeto de semáforo disminuye el recuento del semáforo cada vez que se completa una operación de espera. el subproceso se bloquea cuando el recuento llega a cero. De forma similar, solo el subproceso que posee una exclusión mutua puede llamar correctamente a la función [**ReleaseMutex,**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) aunque cualquier subproceso puede usar [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) para aumentar el recuento de un objeto semáforo.

Un subproceso puede disminuir el recuento de un semáforo más de una vez si se especifica repetidamente el mismo objeto de semáforo en las llamadas a cualquiera de las funciones [de espera](wait-functions.md). Sin embargo, llamar a una de las funciones de espera de varios objetos con una matriz que contiene varios identificadores del mismo semáforo no da lugar a varios decrementos.

Cuando haya terminado de usar el objeto semáforo, llame a la [**función CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) para cerrar el identificador. El objeto semáforo se destruye cuando se cierra su último identificador. Cerrar el identificador no afecta al recuento de semáforos; Por lo tanto, asegúrese de llamar a [**ReleaseSemaphore antes**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) de cerrar el identificador o antes de que finalice el proceso. De lo contrario, las operaciones de espera pendientes pasarán el tiempo de espera o continuarán indefinidamente, dependiendo de si se ha especificado un valor de tiempo de espera.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar objetos semáforos](using-semaphore-objects.md)
</dt> </dl>

 

 
