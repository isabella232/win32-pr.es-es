---
description: Un objeto Semaphore es un objeto de sincronización que mantiene un recuento entre cero y un valor máximo especificado.
ms.assetid: d9da1d98-a306-4e2d-a149-1eef6a724751
title: Objetos Semaphore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a77f36313d76c5d98c786a76f10ad8439965f180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668450"
---
# <a name="semaphore-objects"></a>Objetos Semaphore

Un *objeto Semaphore* es un objeto de sincronización que mantiene un recuento entre cero y un valor máximo especificado. El recuento se reduce cada vez que un subproceso completa una espera para el objeto de semáforo y se incrementa cada vez que un subproceso libera el semáforo. Cuando el recuento llega a cero, ningún subproceso más puede esperar correctamente a que el estado del objeto de semáforo se señale. El estado de un semáforo se establece como señalizado cuando su recuento es mayor que cero y como no señalizado cuando su recuento es cero.

El objeto Semaphore es útil para controlar un recurso compartido que puede admitir un número limitado de usuarios. Actúa como una puerta que limita el número de subprocesos que comparten el recurso a un número máximo especificado. Por ejemplo, una aplicación puede poner un límite en el número de ventanas que crea. Utiliza un semáforo con un recuento máximo igual al límite de la ventana, lo que disminuye el recuento cada vez que se crea una ventana y se incrementa en ella cada vez que se cierra una ventana. La aplicación especifica el objeto Semaphore en la llamada a una de las [funciones de espera](wait-functions.md) antes de que se cree cada ventana. Cuando el recuento es cero (lo que indica que se ha alcanzado el límite de la ventana), la función wait bloquea la ejecución del código de creación de la ventana.

Un subproceso utiliza la función [**createsemaphore (**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea) o [**CreateSemaphoreEx**](/windows/desktop/api/WinBase/nf-winbase-createsemaphoreexa) para crear un objeto Semaphore. El subproceso de creación especifica el recuento inicial y el valor máximo del recuento para el objeto. El recuento inicial no debe ser menor que cero ni mayor que el valor máximo. El subproceso de creación también puede especificar un nombre para el objeto Semaphore. Los subprocesos de otros procesos pueden abrir un identificador de un objeto de semáforo existente especificando su nombre en una llamada a la función [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew) . Para obtener más información sobre los nombres de los objetos mutex, Event, Semaphore y Timer, consulte [sincronización entre procesos](interprocess-synchronization.md).

Si hay más de un subproceso esperando en un semáforo, se selecciona un subproceso en espera. No asuma un orden FIFO (primero en salir, primero en salir). Los eventos externos como APC en modo kernel pueden cambiar el orden de espera.

Cada vez que una de las [funciones de espera](wait-functions.md) se devuelve porque el estado de un semáforo se estableció en señalado, el recuento del semáforo se reduce en uno. La función [**ReleaseSemaphore (**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) aumenta el recuento de un semáforo en una cantidad especificada. El recuento nunca puede ser menor que cero o mayor que el valor máximo.

El recuento inicial de un semáforo normalmente se establece en el valor máximo. El recuento se reduce a partir de ese nivel a medida que se consume el recurso protegido. Como alternativa, puede crear un semáforo con un recuento inicial de cero para bloquear el acceso al recurso protegido mientras se inicializa la aplicación. Después de la inicialización, puede usar [**ReleaseSemaphore (**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) para incrementar el recuento al valor máximo.

Un subproceso que posee un objeto mutex puede esperar varias veces a que el mismo objeto mutex se señale sin que se bloquee su ejecución. Sin embargo, un subproceso que espera varias veces para el mismo objeto de semáforo, disminuye el recuento del semáforo cada vez que se completa una operación de espera; el subproceso se bloquea cuando el número llega a cero. Del mismo modo, solo el subproceso que posee una exclusión mutua puede llamar correctamente a la función [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) , aunque cualquier subproceso puede usar [**ReleaseSemaphore (**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) para aumentar el recuento de un objeto Semaphore.

Un subproceso puede reducir el número de un semáforo más de una vez al especificar repetidamente el mismo objeto de semáforo en las llamadas a cualquiera de las [funciones de espera](wait-functions.md). Sin embargo, al llamar a una de las funciones de espera de varios objetos con una matriz que contiene varios identificadores del mismo semáforo no se producen varios decrementos.

Cuando haya terminado de utilizar el objeto Semaphore, llame a la función [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) para cerrar el controlador. El objeto Semaphore se destruye cuando se ha cerrado su último identificador. Al cerrar el identificador no se ve afectado el recuento del semáforo; por lo tanto, asegúrese de llamar a [**ReleaseSemaphore (**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) antes de cerrar el identificador o antes de que finalice el proceso. De lo contrario, las operaciones de espera pendientes agotarán el tiempo de espera o continuarán de forma indefinida, dependiendo de si se ha especificado un valor de tiempo de espera.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar objetos Semaphore](using-semaphore-objects.md)
</dt> </dl>

 

 
