---
description: Un objeto de sección crítica proporciona una sincronización similar a la que proporciona un objeto de exclusión mutua, salvo que solo los subprocesos de un único proceso pueden usar una sección crítica.
ms.assetid: 2ec11a42-3d12-4d60-9dd7-dc38926d56e1
title: Objetos de sección crítica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbcada1f2ddbc6d370445f36a3dbd51c5c9f54bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667980"
---
# <a name="critical-section-objects"></a>Objetos de sección crítica

Un *objeto de sección crítica* proporciona una sincronización similar a la que proporciona un objeto de exclusión mutua, salvo que solo los subprocesos de un único proceso pueden usar una sección crítica. Los objetos de sección crítica no se pueden compartir entre los procesos.

Los objetos Event, mutex y Semaphore también se pueden usar en una aplicación de un solo proceso, pero los objetos de sección críticos proporcionan un mecanismo ligeramente más rápido y eficaz para la sincronización de exclusión mutua (una prueba específica del procesador y una instrucción set). Al igual que un objeto mutex, un objeto de sección crítica solo puede ser propiedad de un subproceso cada vez, lo que resulta útil para proteger un recurso compartido de acceso simultáneo. A diferencia de un objeto mutex, no hay ninguna manera de saber si se ha abandonado una sección crítica.

A partir de Windows Server 2003 con Service Pack 1 (SP1), los subprocesos que esperan en una sección crítica no adquieren la sección crítica en primer lugar, primero en dar de alta. Este cambio aumenta significativamente el rendimiento de la mayoría de los códigos. Sin embargo, algunas aplicaciones dependen del orden FIFO (el primero en aparecer es el primero en salir) y pueden tener un rendimiento deficiente o no en las versiones actuales de Windows (por ejemplo, las aplicaciones que han estado usando secciones críticas como límite de velocidad). Para asegurarse de que el código sigue funcionando correctamente, puede que tenga que agregar un nivel de sincronización adicional. Por ejemplo, supongamos que tiene un subproceso de productor y un subproceso de consumidor que usan un objeto de sección crítica para sincronizar su trabajo. Cree dos objetos de evento, uno para cada subproceso que se usará para indicar que está listo para que el otro subproceso continúe. El subproceso de consumidor esperará a que el productor señale su evento antes de entrar en la sección crítica, y el subproceso de productor esperará a que el subproceso de consumidor señale su evento antes de entrar en la sección crítica. Una vez que cada subproceso abandona la sección crítica, indica a su evento que libere el otro subproceso.

**Windows Server 2003 y Windows XP:** Los subprocesos que esperan en una sección crítica se agregan a una cola de espera; son reactivarán y generalmente adquieren la sección crítica en el orden en que se agregaron a la cola. Sin embargo, si los subprocesos se agregan a esta cola a una velocidad lo suficientemente rápida, el rendimiento puede degradarse debido al tiempo que se tarda en reactivar cada subproceso en espera.

El proceso es responsable de la asignación de la memoria usada por una sección crítica. Normalmente, esto se realiza simplemente declarando una variable de tipo **crítico \_**. Antes de que los subprocesos del proceso puedan usarlo, inicialice la sección crítica mediante el uso de la función [**InitializeCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsection) o [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) .

Un subproceso utiliza la función [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) o [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) para solicitar la propiedad de una sección crítica. Usa la función [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) para liberar la propiedad de una sección crítica. Si el objeto de sección crítica está siendo propiedad de otro subproceso, **EnterCriticalSection** espera indefinidamente a la propiedad. En cambio, cuando se usa un objeto mutex para la exclusión mutua, las [funciones de espera](wait-functions.md) aceptan un intervalo de tiempo de espera especificado. La función **TryEnterCriticalSection** intenta entrar en una sección crítica sin bloquear el subproceso que realiza la llamada.

Cuando un subproceso posee una sección crítica, puede realizar llamadas adicionales a [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) o [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) sin bloquear su ejecución. Esto evita que un subproceso se interbloquee a sí mismo mientras espera una sección crítica que ya posee. Para liberar su propiedad, el subproceso debe llamar a [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) una vez para cada vez que entró en la sección crítica. No hay ninguna garantía sobre el orden en que los subprocesos en espera adquirirán la propiedad de la sección crítica.

Un subproceso utiliza la función [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) o [**SetCriticalSectionSpinCount**](/windows/win32/api/synchapi/nf-synchapi-setcriticalsectionspincount) para especificar un recuento de giros para el objeto de sección crítica. Girar significa que cuando un subproceso intenta adquirir una sección crítica bloqueada, el subproceso entra en un bucle, comprueba si se libera el bloqueo y, si no se libera el bloqueo, el subproceso entra en suspensión. En los sistemas de un solo procesador, se omite el número de giros y el número de intentos de la sección crítica se establece en 0 (cero). En los sistemas multiprocesador, si la sección crítica no está disponible, el subproceso que realiza la llamada gira *dwSpinCount* veces antes de realizar una operación de espera en un semáforo que está asociado a la sección crítica. Si la sección crítica se vuelve gratuita durante la operación de giro, el subproceso que realiza la llamada evita la operación de espera.

Cualquier subproceso del proceso puede utilizar la función [**DeleteCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-deletecriticalsection) para liberar los recursos del sistema que se asignan cuando se inicializa el objeto de sección crítica. Después de llamar a esta función, no se puede usar el objeto de sección crítica para la sincronización.

Cuando un objeto de sección crítica es propiedad, solo los demás subprocesos afectados son los subprocesos que están a la espera de ser propiedad en una llamada a [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection). Los subprocesos que no están en espera pueden continuar ejecutándose.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos mutex](mutex-objects.md)
</dt> <dt>

[Usar objetos de sección crítica](using-critical-section-objects.md)
</dt> </dl>

 

 
