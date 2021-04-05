---
description: Un objeto mutex es un objeto de sincronización cuyo estado está establecido en señalado cuando no es propiedad de ningún subproceso y no señalizado cuando es propiedad de él.
ms.assetid: eca0795a-1fd0-4034-9d61-9416670919cf
title: Objetos mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e84c17ba3e99e888f7d1e9137a7f24a4d78ce2d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911234"
---
# <a name="mutex-objects"></a>Objetos mutex

Un *objeto mutex* es un objeto de sincronización cuyo estado está establecido en señalado cuando no es propiedad de ningún subproceso y no señalizado cuando es propiedad de él. Solo un subproceso a la vez puede poseer un objeto mutex, cuyo nombre procede del hecho de que es útil para coordinar el acceso mutuamente exclusivo a un recurso compartido. Por ejemplo, para evitar que dos subprocesos escriban en memoria compartida al mismo tiempo, cada subproceso espera a la propiedad de un objeto de exclusión mutua antes de ejecutar el código que tiene acceso a la memoria. Después de escribir en la memoria compartida, el subproceso libera el objeto mutex.

Un subproceso utiliza la función [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) o [**CreateMutexEx**](/windows/win32/api/synchapi/nf-synchapi-createmutexexa) para crear un objeto mutex. El subproceso de creación puede solicitar la propiedad inmediata del objeto mutex y también puede especificar un nombre para el objeto mutex. También puede crear una exclusión mutua sin nombre. Para obtener más información sobre los nombres de los objetos mutex, Event, Semaphore y Timer, consulte [sincronización entre procesos](interprocess-synchronization.md).

Los subprocesos de otros procesos pueden abrir un identificador de un objeto de exclusión mutua con nombre existente especificando su nombre en una llamada a la función [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) . Para pasar un identificador a una exclusión mutua sin nombre a otro proceso, utilice la función [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) o la herencia de controladores de elementos primarios y secundarios.

Cualquier subproceso con un identificador a un objeto mutex puede utilizar una de las [funciones wait](wait-functions.md) para solicitar la propiedad del objeto mutex. Si el objeto mutex es propiedad de otro subproceso, la función wait bloquea el subproceso que hace la solicitud hasta que el subproceso propietario libera el objeto mutex mediante la función [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) . El valor devuelto de la función wait indica si la función devolvió por alguna razón distinta del estado de la exclusión mutua establecida en signald.

Si hay más de un subproceso esperando en una exclusión mutua, se selecciona un subproceso en espera. No asuma un orden FIFO (primero en salir, primero en salir). Los eventos externos como APC en modo kernel pueden cambiar el orden de espera.

Una vez que un subproceso obtiene la propiedad de una exclusión mutua, puede especificar la misma exclusión mutua en llamadas repetidas a las [funciones de espera](wait-functions.md) sin bloquear su ejecución. Esto evita que un subproceso se interbloquee a sí mismo mientras espera una exclusión mutua que ya posee. Para liberar su propiedad en estas circunstancias, el subproceso debe llamar a [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) una vez para cada vez que la exclusión mutua satisfaga las condiciones de una función de espera.

Si un subproceso finaliza sin liberar su propiedad de un objeto mutex, se considera que el objeto mutex está abandonado. Un subproceso en espera puede adquirir la propiedad de un objeto de exclusión mutua abandonada, pero la función wait devolverá **Wait \_ abandonado** para indicar que se ha abandonado el objeto mutex. Un objeto de exclusión mutua abandonada indica que se ha producido un error y que los recursos compartidos protegidos por el objeto mutex están en un estado indefinido. Si el subproceso continúa como si no se hubiera abandonado el objeto mutex, ya no se considera abandonado después de que el subproceso libere su propiedad. Esto restaura el comportamiento normal si un identificador del objeto de exclusión mutua se especifica posteriormente en una función de espera.

Tenga en cuenta que los [objetos de sección crítica](critical-section-objects.md) proporcionan una sincronización similar a la que proporcionan los objetos de exclusión mutua, salvo que los objetos de sección crítica solo los pueden usar los subprocesos de un único proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar objetos mutex](using-mutex-objects.md)
</dt> </dl>

 

 
