---
description: Los puertos de finalización de E/S proporcionan un modelo de subprocesos eficaz para procesar varias solicitudes de E/S asincrónicas en un sistema de varios procesadores.
ms.assetid: 213c48e8-bb21-43ed-9c00-2a5cf8ac25f0
title: Puertos de finalización de E/S
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2133bb14c661580eaf8004bd92c6f947b3b8777a4b1a5f6b330fe631b2be6c81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050835"
---
# <a name="io-completion-ports"></a>Puertos de finalización de E/S

Los puertos de finalización de E/S proporcionan un modelo de subprocesos eficaz para procesar varias solicitudes de E/S asincrónicas en un sistema de varios procesadores. Cuando un proceso crea un puerto de finalización de E/S, el sistema crea un objeto de cola asociado para las solicitudes cuyo único propósito es dar servicio a estas solicitudes. Los procesos que controlan muchas solicitudes de E/S asincrónicas simultáneas pueden hacerlo de forma más rápida y eficaz mediante el uso de puertos de finalización de E/S junto con un grupo de subprocesos asignado previamente que mediante la creación de subprocesos en el momento en que reciben una solicitud de E/S.

## <a name="how-io-completion-ports-work"></a>Cómo funcionan los puertos de finalización de E/S

La [**función CreateIoCompletionPort**](createiocompletionport.md) crea un puerto de finalización de E/S y asocia uno o varios identificadores de archivo a ese puerto. Cuando se completa una operación asincrónica de E/S en uno de estos identificadores de archivo, un paquete de finalización de E/S se pone en cola en orden primero en salir (FIFO) en el puerto de finalización de E/S asociado. Un uso eficaz de este mecanismo es combinar el punto de sincronización de varios identificadores de archivo en un solo objeto, aunque también hay otras aplicaciones útiles. Tenga en cuenta que mientras los paquetes se ponen en cola en orden FIFO, pueden quitarse de la cola en un orden diferente.

> [!Note]
>
> El término *identificador de archivo que* se usa aquí hace referencia a una abstracción del sistema que representa un punto de conexión de E/S superpuesto, no solo un archivo en disco. Por ejemplo, puede ser un punto de conexión de red, un socket TCP, una canalización con nombre o una ranura de correo. Se puede usar cualquier objeto del sistema que admita E/S superpuesta. Para obtener una lista de funciones de E/S relacionadas, vea el final de este tema.

 

Cuando un identificador de archivo está asociado a un puerto de finalización, el bloque de estado pasado no se actualizará hasta que el paquete se quite del puerto de finalización. La única excepción es si la operación original se devuelve sincrónicamente con un error. Un subproceso (ya sea uno creado por el subproceso principal o el propio subproceso principal) usa la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para esperar a que un paquete de finalización se poner en cola en el puerto de finalización de E/S, en lugar de esperar directamente a que se complete la E/S asincrónica. Los subprocesos que bloquean su ejecución en un puerto de finalización de E/S se liberan en orden de último en salir (LIFO) y el siguiente paquete de finalización se extraen de la cola FIFO del puerto de finalización de E/S para ese subproceso. Esto significa que, cuando se libera un paquete de finalización en un subproceso, el sistema libera el último subproceso (más reciente) asociado a ese puerto, y le pasa la información de finalización de la finalización de E/S más antigua.

Aunque cualquier número de subprocesos puede llamar a [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para un puerto de finalización de E/S especificado, cuando un subproceso especificado llama a **GetQueuedCompletionStatus** la primera vez, se asocia al puerto de finalización de E/S especificado hasta que se produce una de estas tres cosas: el subproceso se cierra, especifica un puerto de finalización de E/S diferente o cierra el puerto de finalización de E/S. En otras palabras, un único subproceso se puede asociar, como máximo, a un puerto de finalización de E/S.

Cuando un paquete de finalización se pone en cola en un puerto de finalización de E/S, el sistema comprueba primero cuántos subprocesos asociados a ese puerto se están ejecutando. Si el número de subprocesos que se ejecutan es menor que el valor de simultaneidad (que se describe en la sección siguiente), uno de los subprocesos en espera (el más reciente) puede procesar el paquete de finalización. Cuando un subproceso en ejecución completa su procesamiento, normalmente llama de nuevo a [**GetQueuedCompletionStatus,**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) momento en el que devuelve con el siguiente paquete de finalización o espera si la cola está vacía.

Los subprocesos pueden usar [**la función PostQueuedCompletionStatus para**](postqueuedcompletionstatus.md) colocar paquetes de finalización en la cola de un puerto de finalización de E/S. Al hacerlo, el puerto de finalización se puede usar para recibir comunicaciones de otros subprocesos del proceso, además de recibir paquetes de finalización de E/S del sistema de E/S. La **función PostQueuedCompletionStatus** permite a una aplicación poner en cola sus propios paquetes de finalización de propósito especial en el puerto de finalización de E/S sin iniciar una operación de E/S asincrónica. Esto es útil para notificar a los subprocesos de trabajo eventos externos, por ejemplo.

El identificador de puerto de finalización de E/S y cada identificador de archivo asociado a ese puerto de finalización de E/S determinado se conocen como referencias al puerto de finalización *de E/S*. El puerto de finalización de E/S se libera cuando no hay más referencias a él. Por lo tanto, todos estos identificadores deben cerrarse correctamente para liberar el puerto de finalización de E/S y sus recursos del sistema asociados. Una vez que se cumplen estas condiciones, una aplicación debe cerrar el identificador del puerto de finalización de E/S llamando a la [**función CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)

> [!Note]
>
> Un puerto de finalización de E/S está asociado al proceso que lo creó y no se puede compartir entre procesos. Sin embargo, un único identificador se puede compartir entre subprocesos en el mismo proceso.

 

## <a name="threads-and-concurrency"></a>Subprocesos y simultaneidad

La propiedad más importante de un puerto de finalización de E/S que se debe tener en cuenta detenidamente es el valor de simultaneidad. El valor de simultaneidad de un puerto de finalización se especifica cuando se crea con [**CreateIoCompletionPort**](createiocompletionport.md) mediante el *parámetro NumberOfConcurrentThreads.* Este valor limita el número de subprocesos que se pueden ejecutar asociados al puerto de finalización. Cuando el número total de subprocesos que se pueden ejecutar asociados al puerto de finalización alcanza el valor de simultaneidad, el sistema bloquea la ejecución de los subprocesos subsiguientes asociados a ese puerto de finalización hasta que el número de subprocesos ejecutables cae por debajo del valor de simultaneidad.

El escenario más eficaz se produce cuando hay paquetes de finalización en espera en la cola, pero no se pueden satisfacer las esperas porque el puerto ha alcanzado su límite de simultaneidad. Tenga en cuenta lo que sucede con un valor de simultaneidad de uno y varios subprocesos que esperan en la llamada de función [**GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) En este caso, si la cola siempre tiene paquetes de finalización en espera, cuando el subproceso en ejecución llama a **GetQueuedCompletionStatus**, no bloqueará la ejecución porque, como se mencionó anteriormente, la cola de subprocesos es LIFO. En su lugar, este subproceso recogerá inmediatamente el siguiente paquete de finalización en cola. No se producirá ningún cambio de contexto de subproceso, porque el subproceso en ejecución está seleccionando continuamente paquetes de finalización y los demás subprocesos no se pueden ejecutar.

> [!Note]
>
> En el ejemplo anterior, los subprocesos adicionales parecen ser inutiles y nunca se ejecutan, pero eso supone que el subproceso en ejecución nunca se pone en estado de espera por algún otro mecanismo, finaliza o cierra de otro modo su puerto de finalización de E/S asociado. Tenga en cuenta todas estas ramificaciones de ejecución de subprocesos al diseñar la aplicación.

 

El mejor valor máximo general para elegir para el valor de simultaneidad es el número de CPU en el equipo. Si la transacción requiere un cálculo largo, un valor de simultaneidad mayor permitirá que se ejecuten más subprocesos. Cada paquete de finalización puede tardar más tiempo en finalizar, pero se procesarán más paquetes de finalización al mismo tiempo. Puede experimentar con el valor de simultaneidad junto con las herramientas de generación de perfiles para lograr el mejor efecto para la aplicación.

El sistema también permite que un subproceso que espera en [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) procese un paquete de finalización si otro subproceso en ejecución asociado al mismo puerto de finalización de E/S entra en estado de espera por otros motivos, por ejemplo, la [**función SuspendThread.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-suspendthread) Cuando el subproceso en estado de espera comienza a ejecutarse de nuevo, puede haber un breve período en el que el número de subprocesos activos supere el valor de simultaneidad. Sin embargo, el sistema reduce rápidamente este número al no permitir nuevos subprocesos activos hasta que el número de subprocesos activos esté por debajo del valor de simultaneidad. Este es un motivo para que la aplicación cree más subprocesos en su grupo de subprocesos que el valor de simultaneidad. La administración del grupo de subprocesos está fuera del ámbito de este tema, pero una buena regla general es tener un mínimo del doble de subprocesos en el grupo de subprocesos que hay procesadores en el sistema. Para obtener información adicional sobre la agrupación de subprocesos, vea [Grupos de subprocesos](/windows/desktop/ProcThread/thread-pools).

## <a name="supported-io-functions"></a>Funciones de E/S admitidas

Las siguientes funciones se pueden usar para iniciar operaciones de E/S que se completan mediante puertos de finalización de E/S. Debe pasar a la función una instancia de la estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) y un identificador de archivo previamente asociado a un puerto de finalización de E/S (mediante una llamada a [**CreateIoCompletionPort**](createiocompletionport.md)) para habilitar el mecanismo de puerto de finalización de E/S:

-   [**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
-   [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
-   [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
-   [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
-   [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
-   [**TransactNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
-   [**WaitCommEvent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
-   [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
-   [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
-   [**WSASendTo**](/windows/desktop/api/winsock2/nf-winsock2-wsasendto)
-   [**WSASend**](/windows/desktop/api/winsock2/nf-winsock2-wsasend)
-   [**WSARecvFrom**](/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom)
-   [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
-   [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>


</dt> <dt>

[Acerca de los procesos y los subprocesos](/windows/desktop/ProcThread/about-processes-and-threads)
</dt> <dt>

[**BindIoCompletionCallback**](/windows/desktop/api/winbase/nf-winbase-bindiocompletioncallback)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> </dl>

 

 
