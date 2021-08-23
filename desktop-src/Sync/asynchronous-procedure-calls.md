---
description: Una llamada a procedimiento asincrónico (APC) es una función que se ejecuta de forma asincrónica en el contexto de un subproceso determinado.
ms.assetid: 0197d78e-a4dc-414b-88ba-c5ec5f2ed614
title: Llamadas a procedimiento asincrónico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c024506c2afc9a895db645fd386ed76f915f6e1178c6b8ce3a257aa7d40fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661455"
---
# <a name="asynchronous-procedure-calls"></a>Llamadas a procedimiento asincrónico

Una *llamada a procedimiento asincrónico* (APC) es una función que se ejecuta de forma asincrónica en el contexto de un subproceso determinado. Cuando un APC se pone en cola en un subproceso, el sistema emite una interrupción de software. La próxima vez que se programe el subproceso, ejecutará la función APC. Un APC generado por el sistema se denomina *APC en modo kernel.* Un APC generado por una aplicación se denomina *APC en modo de usuario.* Un subproceso debe estar en un estado de alerta para ejecutar un APC en modo de usuario.

Cada subproceso tiene su propia cola de APC. Una aplicación pone en cola un APC a un subproceso mediante una llamada a la [**función QueueUserAPC.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queueuserapc) El subproceso que realiza la llamada especifica la dirección de una función de APC en la llamada a **QueueUserAPC**. La cola de un APC es una solicitud para que el subproceso llame a la función APC.

Cuando se pone en cola un APC en modo de usuario, no se dirige al subproceso al que se pone en cola para llamar a la función APC a menos que esté en estado de alerta. Un subproceso entra en un estado de alerta cuando llama a la función [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), [**SignalObjectAndWait,**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) [**MsgWaitForMultipleObjectsEx,**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) [**WaitForMultipleObjectsEx**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjectsex)o [**WaitForSingleObjectEx.**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) Si se cumple la espera antes de poner en cola el APC, el subproceso ya no se encuentra en un estado de espera que se puede alertar, por lo que no se ejecutará la función APC. Sin embargo, el APC sigue en cola, por lo que la función APC se ejecutará cuando el subproceso llame a otra función de espera que se pueda alertar.

Las funciones [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex), [**SetWaitableTimer,**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)y [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex) se implementan mediante un APC como mecanismo de devolución de llamada de notificación de finalización.

Si usa un grupo de subprocesos [,](../procthread/thread-pools.md)tenga en cuenta que las API no funcionan así como otros mecanismos de señalización porque el sistema controla la duración de los subprocesos del grupo de subprocesos, por lo que es posible que un subproceso finalice antes de que se entregue la notificación. En lugar de usar un mecanismo de señalización basado en APC, como el parámetro *pfnCompletionRoutine* de [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) o [**SetWaitableTimerEx,**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)use un objeto que se puede esperar, como un temporizador creado con [**CreateThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer). Para E/S, use un objeto de finalización de E/S creado con [**CreateThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio) o una estructura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) basada en *hEvent* donde el evento se pueda pasar a la [**función SetThreadpoolWait.**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait)

## <a name="synchronization-internals"></a>Información interna de sincronización

Cuando se emite una solicitud de E/S, se asigna una estructura para representar la solicitud. Esta estructura se denomina paquete de solicitud de E/S (IRP). Con la E/S sincrónica, el subproceso compila el IRP, lo envía a la pila de dispositivos y espera en el kernel a que se complete el IRP. Con la E/S asincrónica, el subproceso compila el IRP y lo envía a la pila de dispositivos. La pila podría completar el IRP inmediatamente o podría devolver un estado pendiente que indica que la solicitud está en curso. Cuando esto sucede, el IRP sigue asociado al subproceso, por lo que se cancelará si el subproceso finaliza o llama a una función como [**CancelIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelio). Mientras tanto, el subproceso puede seguir haciendo otras tareas mientras la pila de dispositivos sigue procesando el IRP.

Hay varias maneras en que el sistema puede indicar que el IRP se ha completado:

-   Actualice la estructura superpuesta con el resultado de la operación para que el subproceso pueda sondear para determinar si la operación se ha completado.
-   Señale el evento en la estructura superpuesta para que un subproceso pueda sincronizarse en el evento y ser resonado cuando se complete la operación.
-   Poner en cola el IRP en el APC pendiente del subproceso para que el subproceso ejecute la rutina APC cuando entre en un estado de espera de alerta y vuelva de la operación de espera con un estado que indica que ejecutó una o varias rutinas de APC.
-   Poner en cola el IRP en un puerto de finalización de E/S, donde lo ejecutará el siguiente subproceso que espera en el puerto de finalización.

Los subprocesos que esperan en un puerto de finalización de E/S no esperan en estado de alerta. Por lo tanto, si esos subprocesos emiten IRP que están configurados para completarse como API para el subproceso, esas finalizaciones de IPC no se producirán de forma oportuna; solo se producirán si el subproceso toma una solicitud del puerto de finalización de E/S y, a continuación, entra en una espera que se puede alertar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar un temporizador que se puede esperar con una llamada a procedimiento asincrónico](using-a-waitable-timer-with-an-asynchronous-procedure-call.md)
</dt> </dl>

 

 
