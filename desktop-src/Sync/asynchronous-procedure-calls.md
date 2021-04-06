---
description: Una llamada a procedimiento asincrónico (APC) es una función que se ejecuta de forma asincrónica en el contexto de un subproceso determinado.
ms.assetid: 0197d78e-a4dc-414b-88ba-c5ec5f2ed614
title: Llamadas a procedimientos asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd95e9afd663e2a462335b3c47bfe99462b449e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002461"
---
# <a name="asynchronous-procedure-calls"></a>Llamadas a procedimientos asincrónicos

Una *llamada a procedimiento asincrónico* (APC) es una función que se ejecuta de forma asincrónica en el contexto de un subproceso determinado. Cuando un APC se pone en cola en un subproceso, el sistema emite una interrupción de software. La próxima vez que se programe el subproceso, se ejecutará la función APC. Una APC generada por el sistema se denomina *APC en modo kernel*. Una APC generada por una aplicación se denomina *APC de modo usuario*. Un subproceso debe estar en un estado de alerta para ejecutar un APC en modo de usuario.

Cada subproceso tiene su propia cola APC. Una aplicación pone en cola un APC en un subproceso llamando a la función [**QueueUserAPC**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queueuserapc) . El subproceso que realiza la llamada especifica la dirección de una función APC en la llamada a **QueueUserAPC**. La puesta en cola de una APC es una solicitud para que el subproceso llame a la función APC.

Cuando se pone en cola un APC en modo de usuario, el subproceso al que se pone en cola no se dirige para llamar a la función APC a menos que esté en un estado de alerta. Un subproceso entra en un estado de alerta cuando llama a la función [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex), [**WaitForMultipleObjectsEx**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjectsex)o [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) . Si se cumple la espera antes de que se haya puesto en cola el APC, el subproceso ya no se encuentra en un estado de espera de alerta, por lo que la función APC no se ejecutará. Sin embargo, el APC todavía se pone en la cola, por lo que la función APC se ejecutará cuando el subproceso llame a otra función de espera de alerta.

Las funciones [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex), [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer), [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)y [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex) se implementan mediante una APC como el mecanismo de devolución de llamada de notificación de finalización.

Si usa un grupo de [subprocesos](../procthread/thread-pools.md), tenga en cuenta que APC no funcionan así como otros mecanismos de señalización porque el sistema controla la duración de los subprocesos del grupo de subprocesos, por lo que es posible que un subproceso finalice antes de que se entregue la notificación. En lugar de usar un mecanismo de señalización basado en APC como el parámetro *pfnCompletionRoutine* de [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) o [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex), use un objeto que se debe esperar, como un temporizador creado con [**CreateThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer). En e/s, use un objeto de finalización de e/s creado con [**CreateThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio) o una estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) basada en *hEvent* en la que se pueda pasar el evento a la función [**SetThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait) .

## <a name="synchronization-internals"></a>Mecanismos internos de sincronización

Cuando se emite una solicitud de e/s, se asigna una estructura para representar la solicitud. Esta estructura se denomina paquete de solicitud de e/s (IRP). Con la e/s sincrónica, el subproceso compila el IRP, lo envía a la pila del dispositivo y espera en el kernel para que se complete el IRP. Con la e/s asincrónica, el subproceso compila el IRP y lo envía a la pila del dispositivo. La pila podría completar el IRP inmediatamente o podría devolver un estado pendiente que indica que la solicitud está en curso. Cuando esto sucede, el IRP todavía está asociado al subproceso, por lo que se cancelará si el subproceso finaliza o llama a una función como [**CancelIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelio). Mientras tanto, el subproceso puede continuar realizando otras tareas mientras la pila de dispositivos continúa procesando el IRP.

Hay varias maneras en las que el sistema puede indicar que se ha completado el IRP:

-   Actualice la estructura superpuesta con el resultado de la operación para que el subproceso pueda realizar un sondeo para determinar si la operación se ha completado.
-   Señale el evento en la estructura superpuesta para que un subproceso pueda sincronizarse en el evento y ser reactivarán cuando se complete la operación.
-   Ponga en cola el IRP en el APC pendiente del subproceso para que el subproceso ejecute la rutina APC cuando entre en un estado de espera de alerta y vuelva de la operación de espera con un estado que indique que ejecutó una o más rutinas APC.
-   Pone en cola el IRP en un puerto de finalización de e/s, donde lo ejecutará el siguiente subproceso que espera en el puerto de finalización.

Los subprocesos que esperan en un puerto de finalización de e/s no esperan en un estado de alerta. Por lo tanto, si esos subprocesos emiten IRP que se establecen para completarse como APC en el subproceso, esas finalizaciones de IPC no se realizarán de manera oportuna; solo se producirán si el subproceso recoge una solicitud del puerto de finalización de e/s y, a continuación, entra en una espera de alerta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar un temporizador que se debe esperar con una llamada a procedimiento asincrónica](using-a-waitable-timer-with-an-asynchronous-procedure-call.md)
</dt> </dl>

 

 
