---
description: Los puertos de finalización de e/s proporcionan un modelo de subprocesos eficaz para procesar varias solicitudes de e/s asincrónicas en un sistema de varios procesadores.
ms.assetid: 213c48e8-bb21-43ed-9c00-2a5cf8ac25f0
title: Puertos de finalización de e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 882363ef99821a0b0b40810f45d609c5b5f7760c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669690"
---
# <a name="io-completion-ports"></a>Puertos de finalización de e/s

Los puertos de finalización de e/s proporcionan un modelo de subprocesos eficaz para procesar varias solicitudes de e/s asincrónicas en un sistema de varios procesadores. Cuando un proceso crea un puerto de finalización de e/s, el sistema crea un objeto de cola asociado para las solicitudes cuyo único propósito es atender estas solicitudes. Los procesos que administran muchas solicitudes de e/s asincrónicas simultáneas pueden hacerlo de manera más rápida y eficaz mediante puertos de finalización de e/s junto con un grupo de subprocesos previamente asignados que al crear subprocesos en el momento en que reciben una solicitud de e/s.

## <a name="how-io-completion-ports-work"></a>Cómo funcionan los puertos de finalización de e/s

La función [**CreateIoCompletionPort**](createiocompletionport.md) crea un puerto de finalización de e/s y asocia uno o más identificadores de archivo a ese puerto. Cuando se completa una operación de e/s asincrónica en uno de estos identificadores de archivo, un paquete de finalización de e/s se pone en cola en el orden FIFO (el primero en salir es el primero en salir) al puerto de terminación de e/s asociado. Un uso eficaz de este mecanismo es combinar el punto de sincronización para varios identificadores de archivo en un solo objeto, aunque también hay otras aplicaciones útiles. Tenga en cuenta que, mientras los paquetes se ponen en cola en orden FIFO, se pueden quitar de la cola en un orden diferente.

> [!Note]
>
> El término *identificador de archivo* tal como se usa aquí hace referencia a una abstracción del sistema que representa un punto de conexión de e/s superpuesto, no solo un archivo en disco. Por ejemplo, puede ser un punto de conexión de red, un socket TCP, una canalización con nombre o una ranura de correo. Se puede usar cualquier objeto del sistema que admita e/s superpuesta. Para obtener una lista de las funciones de e/s relacionadas, consulte el final de este tema.

 

Cuando un identificador de archivo está asociado a un puerto de finalización, el bloque de estado que se pasa no se actualizará hasta que el paquete se quite del puerto de finalización. La única excepción es si la operación original vuelve sincrónicamente con un error. Un subproceso (uno creado por el subproceso principal o el propio subproceso principal) utiliza la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para esperar a que un paquete de finalización se encuentre en la cola del puerto de finalización de e/s, en lugar de esperar directamente a que se complete la e/s asincrónica. Los subprocesos que bloquean su ejecución en un puerto de finalización de e/s se liberan en orden LIFO (último en salir, primero en salir) y el siguiente paquete de finalización se extrae de la cola FIFO del puerto de finalización de e/s para ese subproceso. Esto significa que, cuando se publica un paquete de finalización en un subproceso, el sistema libera el último subproceso (más reciente) asociado a ese puerto y lo pasa a la información de finalización de la finalización de e/s más antigua.

Aunque cualquier número de subprocesos puede llamar a [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para un puerto de terminación de e/s especificado, cuando un subproceso especificado llama a **GetQueuedCompletionStatus** la primera vez, se asocia con el puerto de finalización de e/s especificado hasta que se produce una de tres cosas: el subproceso se cierra, especifica un puerto de finalización de e/s diferente o cierra el puerto de finalización En otras palabras, un único subproceso se puede asociar a un puerto de finalización de e/s como máximo.

Cuando un paquete de finalización se pone en cola en un puerto de finalización de e/s, el sistema comprueba primero cuántos subprocesos asociados a ese puerto se están ejecutando. Si el número de subprocesos que se ejecutan es menor que el valor de simultaneidad (descrito en la sección siguiente), se permite que uno de los subprocesos en espera (el más reciente) Procese el paquete de finalización. Cuando un subproceso en ejecución completa su procesamiento, normalmente llama de nuevo a [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) , momento en el que se devuelve con el siguiente paquete de finalización o espera si la cola está vacía.

Los subprocesos pueden usar la función [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) para colocar los paquetes de finalización en la cola de un puerto de finalización de e/s. Al hacerlo, el puerto de finalización se puede usar para recibir comunicaciones de otros subprocesos del proceso, además de recibir paquetes de finalización de e/s del sistema de e/s. La función **PostQueuedCompletionStatus** permite a una aplicación poner en cola sus propios paquetes de finalización especial en el puerto de finalización de e/s sin iniciar una operación de e/s asincrónica. Esto es útil para notificar a los subprocesos de trabajo de eventos externos, por ejemplo.

El identificador de puerto de finalización de e/s y todos los identificadores de archivo asociados a ese puerto de terminación de e/s concreto se conocen como *referencias al puerto de terminación de e/s*. El puerto de finalización de e/s se libera cuando no hay más referencias a él. Por lo tanto, todos estos identificadores deben estar cerrados correctamente para liberar el puerto de finalización de e/s y sus recursos del sistema asociados. Una vez que se cumplen estas condiciones, una aplicación debe cerrar el identificador del puerto de finalización de e/s mediante una llamada a la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .

> [!Note]
>
> Un puerto de finalización de e/s está asociado al proceso que lo creó y no se puede compartir entre los procesos. Sin embargo, un único identificador se compartirá entre los subprocesos del mismo proceso.

 

## <a name="threads-and-concurrency"></a>Subprocesos y simultaneidad

La propiedad más importante de un puerto de finalización de e/s que se debe considerar con cuidado es el valor de simultaneidad. El valor de simultaneidad de un puerto de finalización se especifica cuando se crea con [**CreateIoCompletionPort**](createiocompletionport.md) a través del parámetro *NumberOfConcurrentThreads* . Este valor limita el número de subprocesos ejecutables asociados al puerto de finalización. Cuando el número total de subprocesos ejecutables asociados al puerto de finalización alcanza el valor de simultaneidad, el sistema bloquea la ejecución de los subprocesos posteriores asociados a ese puerto de finalización hasta que el número de subprocesos ejecutables caiga por debajo del valor de simultaneidad.

El escenario más eficaz se produce cuando hay paquetes de finalización en espera en la cola, pero no se puede satisfacer ninguna espera porque el puerto ha alcanzado su límite de simultaneidad. Tenga en cuenta lo que sucede con un valor de simultaneidad de uno y varios subprocesos que esperan en la llamada de función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) . En este caso, si la cola siempre tiene paquetes de finalización en espera, cuando el subproceso en ejecución llama a **GetQueuedCompletionStatus**, no bloqueará la ejecución porque, como se mencionó anteriormente, la cola de subprocesos es LIFO. En su lugar, este subproceso recogerá inmediatamente el siguiente paquete de finalización en cola. No se producirán cambios de contexto de subproceso, ya que el subproceso en ejecución selecciona continuamente los paquetes de finalización y los demás subprocesos no se pueden ejecutar.

> [!Note]
>
> En el ejemplo anterior, los subprocesos adicionales parecen ser inútiles y no ejecutarse, pero eso supone que el subproceso en ejecución nunca se pone en un estado de espera por algún otro mecanismo, finaliza o cierra su puerto de finalización de e/s asociado. Tenga en cuenta todas esas ramificaciones de ejecución de subprocesos al diseñar la aplicación.

 

El mejor valor máximo general para elegir para el valor de simultaneidad es el número de CPU del equipo. Si la transacción requirió un cálculo largo, un valor de simultaneidad mayor permitirá que se ejecuten más subprocesos. Cada paquete de finalización puede tardar más tiempo en completarse, pero se procesarán más paquetes de finalización al mismo tiempo. Puede experimentar con el valor de simultaneidad junto con las herramientas de generación de perfiles para lograr el mejor efecto para su aplicación.

El sistema también permite que un subproceso que espera en [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) procese un paquete de finalización si otro subproceso en ejecución asociado con el mismo puerto de finalización de e/s entra en un estado de espera por otros motivos, por ejemplo, la función [**SuspendThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-suspendthread) . Cuando el subproceso en el estado de espera empieza a ejecutarse de nuevo, puede haber un breve período en el que el número de subprocesos activos supera el valor de simultaneidad. Sin embargo, el sistema reduce rápidamente este número al no permitir ningún subproceso activo nuevo hasta que el número de subprocesos activos caiga por debajo del valor de simultaneidad. Esta es una de las razones para que la aplicación cree más subprocesos en su grupo de subprocesos que el valor de simultaneidad. La administración de grupos de subprocesos queda fuera del ámbito de este tema, pero una buena regla general es tener un mínimo de dos subprocesos en el grupo de subprocesos, ya que hay procesadores en el sistema. Para obtener más información sobre la agrupación de subprocesos, vea [grupos de subprocesos](/windows/desktop/ProcThread/thread-pools).

## <a name="supported-io-functions"></a>Funciones de e/s admitidas

Las siguientes funciones se pueden usar para iniciar operaciones de e/s que se completan mediante puertos de finalización de e/s. Debe pasar la función a una instancia de la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) y a un identificador de archivo asociado previamente a un puerto de finalización de e/s (mediante una llamada a [**CreateIoCompletionPort**](createiocompletionport.md)) para habilitar el mecanismo del puerto de finalización de e/s:

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

 

 
