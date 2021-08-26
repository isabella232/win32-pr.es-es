---
description: La programación en modo de usuario (UMS) es un mecanismo ligero que las aplicaciones pueden usar para programar sus propios subprocesos.
ms.assetid: f9dd92fe-6d7a-452c-893e-e6df1757e377
title: User-Mode programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a13b30685dbcbfc4d3d502e02bdbfdc10d15ea1f804cc6a8391073c44ce447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074245"
---
# <a name="user-mode-scheduling"></a>User-Mode programación

La programación en modo de usuario (UMS) es un mecanismo ligero que las aplicaciones pueden usar para programar sus propios subprocesos. Una aplicación puede cambiar entre subprocesos UMS [](scheduling.md) en modo de usuario sin implicar al programador del sistema y recuperar el control del procesador si un subproceso UMS se bloquea en el kernel. Los subprocesos UMS difieren de las [fibras](fibers.md) en que cada subproceso UMS tiene su propio contexto de subproceso en lugar de compartir el contexto de subproceso de un único subproceso. La capacidad de cambiar entre subprocesos en [](thread-pools.md) modo de usuario hace que UMS sea más eficaz que los grupos de subprocesos para administrar un gran número de elementos de trabajo de corta duración que requieren pocas llamadas del sistema.

UMS se recomienda para aplicaciones con requisitos de alto rendimiento que necesitan ejecutar eficazmente muchos subprocesos simultáneamente en sistemas multiprocesador o de varios núcleos. Para aprovechar las ventajas de UMS, una aplicación debe implementar un componente de programador que administre los subprocesos UMS de la aplicación y determine cuándo deben ejecutarse. Los desarrolladores deben considerar si sus requisitos de rendimiento de aplicaciones justifican el trabajo implicado en el desarrollo de este tipo de componente. Es posible que las aplicaciones con requisitos de rendimiento moderados se atendidas mejor al permitir que el programador del sistema programe sus subprocesos.

UMS está disponible para aplicaciones de 64 bits que se ejecutan en versiones de 64 bits de Windows 7 y Windows Server 2008 R2 o versiones posteriores de 64 bits de Windows. Esta característica no está disponible en versiones de 32 bits de Windows.

Para más información, consulte las secciones siguientes:

-   [Programador ums](#ums-scheduler)
-   [Subproceso del programador ums](#ums-scheduler-thread)
-   [Subprocesos de trabajo ums, contextos de subproceso y listas de finalización](#ums-worker-threads-thread-contexts-and-completion-lists)
-   [Función de punto de entrada del programador ums](#ums-scheduler-entry-point-function)
-   [Ejecución de subprocesos UMS](#ums-thread-execution)
-   [Procedimientos recomendados de UMS](#ums-best-practices)

## <a name="ums-scheduler"></a>Programador ums

El programador ums de una aplicación es responsable de crear, administrar y eliminar subprocesos UMS y determinar qué subproceso ums se va a ejecutar. El programador de una aplicación realiza las siguientes tareas:

-   Crea un subproceso de programador ums para cada procesador en el que la aplicación ejecutará subprocesos de trabajo UMS.
-   Crea subprocesos de trabajo UMS para realizar el trabajo de la aplicación.
-   Mantiene su propia cola de subprocesos de trabajo lista para ejecutarse y selecciona los subprocesos que se van a ejecutar en función de las directivas de programación de la aplicación.
-   Crea y supervisa una o varias listas de finalización en las que el sistema pone en cola los subprocesos después de finalizar el procesamiento en el kernel. Estos incluyen subprocesos de trabajo recién creados y subprocesos bloqueados previamente en una llamada del sistema que se desbloquea.
-   Proporciona una función de punto de entrada del programador para que controle las notificaciones del sistema. El sistema llama a la función de punto de entrada cuando se crea un subproceso de programador, cuando un subproceso de trabajo se bloquea en una llamada del sistema o cuando un subproceso de trabajo produce el control explícitamente.
-   Realiza tareas de limpieza para subprocesos de trabajo que han terminado de ejecutarse.
-   Realiza un apagado orden del programador cuando lo solicita la aplicación.

## <a name="ums-scheduler-thread"></a>Subproceso del programador ums

Un subproceso del programador UMS es un subproceso normal que se ha convertido a UMS llamando a la [**función EnterUmsSchedulingMode.**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) El programador del sistema determina cuándo se ejecuta el subproceso del programador UMS en función de su prioridad con respecto a otros subprocesos listos. El procesador en el que se ejecuta el subproceso del programador se ve afectado por la afinidad del subproceso, igual que para los subprocesos que no son UMS.

El llamador [**de EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) especifica una lista de finalización y una función de punto de entrada [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) que se va a asociar al subproceso del programador ums. El sistema llama a la función de punto de entrada especificada cuando termina de convertir el subproceso que realiza la llamada a UMS. La función de punto de entrada del programador es responsable de determinar la siguiente acción adecuada para el subproceso especificado. Para obtener más información, vea [UmS Scheduler Entry Point Function](#ums-scheduler-entry-point-function) más adelante en este tema.

Una aplicación podría crear un subproceso de programador UMS para cada procesador que se usará para ejecutar subprocesos UMS. La aplicación también podría establecer la afinidad de cada subproceso del programador UMS para un procesador lógico específico, que tiende a excluir subprocesos no relacionados de la ejecución en ese procesador, reservando eficazmente para ese subproceso del programador. Tenga en cuenta que establecer la afinidad de subprocesos de esta manera puede afectar al rendimiento general del sistema al agotar otros procesos que pueden estar ejecutándose en el sistema. Para obtener más información sobre la afinidad de subprocesos, [vea Varios procesadores.](multiple-processors.md)

## <a name="ums-worker-threads-thread-contexts-and-completion-lists"></a>Subprocesos de trabajo ums, contextos de subproceso y listas de finalización

Se crea un subproceso de trabajo UMS llamando a [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) con el atributo PROC THREAD ATTRIBUTE UMS THREAD y especificando un contexto de subproceso UMS y una lista \_ \_ de \_ \_ finalización.

Un contexto de subproceso UMS representa el estado del subproceso UMS de un subproceso de trabajo y se usa para identificar el subproceso de trabajo en las llamadas de función UMS. Se crea mediante una llamada [**a CreateUmsThreadContext.**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)

Se crea una lista de finalización mediante una llamada a [**la función CreateUmsCompletionList.**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist) Una lista de finalización recibe subprocesos de trabajo UMS que han completado la ejecución en el kernel y están listos para ejecutarse en modo de usuario. Solo el sistema puede poner en cola los subprocesos de trabajo en una lista de finalización. Los nuevos subprocesos de trabajo UMS se ponen automáticamente en cola en la lista de finalización especificada cuando se crearon los subprocesos. Los subprocesos de trabajo bloqueados anteriormente también se ponen en cola en la lista de finalización cuando ya no están bloqueados.

Cada subproceso del programador ums está asociado a una lista de finalización única. Sin embargo, la misma lista de finalización se puede asociar a cualquier número de subprocesos del programador UMS y un subproceso de programador puede recuperar contextos UMS de cualquier lista de finalización para la que tenga un puntero.

Cada lista de finalización tiene un evento asociado que el sistema señala cuando pone en cola uno o varios subprocesos de trabajo en una lista vacía. La [**función GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent) recupera un identificador para el evento para una lista de finalización especificada. Una aplicación puede esperar en más de un evento de lista de finalización junto con otros eventos que tienen sentido para la aplicación.

## <a name="ums-scheduler-entry-point-function"></a>Función de punto de entrada del programador ums

La función de punto de entrada del programador de una aplicación se implementa como una [*función UmsSchedulerProc.*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) El sistema llama a la función de punto de entrada del programador de la aplicación en las siguientes ocasiones:

-   Cuando un subproceso que no es UMS se convierte en un subproceso del programador ums llamando a [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode).
-   Cuando un subproceso de trabajo de UMS llama a [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield).
-   Cuando un subproceso de trabajo ums se bloquea en un servicio del sistema, como una llamada del sistema o un error de página.

El *parámetro Reason* de la función [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) especifica el motivo por el que se llamó a la función de punto de entrada. Si se llamó a la función de punto de entrada porque se creó un nuevo subproceso de programador UMS, el parámetro *SchedulerParam* contiene los datos especificados por el autor de la llamada de [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode). Si se llamó a la función de punto de entrada porque se produjo un subproceso de trabajo UMS, el parámetro *SchedulerParam* contiene los datos especificados por el autor de la llamada de [**UmsThreadYield.**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield) Si se llamó a la función de punto de entrada porque un subproceso de trabajo UMS se bloqueó en el kernel, el parámetro *SchedulerParam* es NULL.

La función de punto de entrada del programador es responsable de determinar la siguiente acción adecuada para el subproceso especificado. Por ejemplo, si se bloquea un subproceso de trabajo, la función de punto de entrada del programador podría ejecutar el siguiente subproceso de trabajo UMS listo disponible.

Cuando se llama a la función de punto de entrada del programador, el programador de la aplicación debe intentar recuperar todos los elementos de su lista de finalización asociada llamando a la función [**DequeueUmsCompletionListItems.**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) Esta función recupera una lista de contextos de subproceso UMS que han terminado de procesarse en el kernel y están listos para ejecutarse en modo de usuario. El programador de la aplicación no debe ejecutar subprocesos UMS directamente desde esta lista porque esto puede provocar un comportamiento impredecible en la aplicación. En su lugar, el programador debe recuperar todos los contextos de subproceso UMS llamando a la función [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem) una vez para cada contexto, insertar los contextos de subproceso UMS en la cola de subprocesos preparada del programador y, a continuación, ejecutar solo los subprocesos UMS desde la cola de subprocesos lista.

Si el programador no necesita esperar varios eventos, debe llamar a [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) con un parámetro de tiempo de espera distinto de cero para que la función espere en el evento de lista de finalización antes de volver. Si el programador necesita esperar varios eventos de lista de finalización, debe llamar a **DequeueUmsCompletionListItems** con un parámetro timeout de cero para que la función se devuelva inmediatamente, incluso si la lista de finalización está vacía. En este caso, el programador puede esperar explícitamente los eventos de lista de finalización, por ejemplo, mediante [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects).

## <a name="ums-thread-execution"></a>Ejecución de subprocesos UMS

Un subproceso de trabajo UMS recién creado se pone en cola en la lista de finalización especificada y no comienza a ejecutarse hasta que el programador ums de la aplicación lo selecciona para ejecutarse. Esto difiere de los subprocesos que no son UMS, que el programador del sistema programa automáticamente para ejecutarse a menos que el autor de la llamada cree explícitamente el subproceso suspendido.

El programador ejecuta un subproceso de trabajo llamando [**a ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread) con el contexto UMS del subproceso de trabajo. Un subproceso de trabajo ums se ejecuta hasta que se produce llamando a la función [**UmsThreadYield,**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield) bloquea o finaliza.

## <a name="ums-best-practices"></a>Procedimientos recomendados de UMS

Las aplicaciones que implementan UMS deben seguir estos procedimientos recomendados:

-   El sistema administra las estructuras subyacentes para los contextos de subproceso UMS y no se deben modificar directamente. En su lugar, use [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation) y [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation) para recuperar y establecer información sobre un subproceso de trabajo UMS.
-   Para ayudar a evitar interbloqueos, el subproceso del programador ums no debe compartir bloqueos con subprocesos de trabajo ums. Esto incluye bloqueos creados por la aplicación y bloqueos del sistema adquiridos indirectamente por operaciones como la asignación desde el montón o la carga de archivos DLL. Por ejemplo, suponga que el programador ejecuta un subproceso de trabajo UMS que carga un archivo DLL. El subproceso de trabajo adquiere el bloqueo y los bloques del cargador. El sistema llama a la función de punto de entrada del programador, que luego carga un archivo DLL. Esto provoca un interbloqueo, porque el bloqueo del cargador ya se mantiene y no se puede liberar hasta que se desbloquea el primer subproceso. Para evitar este problema, delegue el trabajo que podría compartir bloqueos con subprocesos de trabajo UMS en un subproceso de trabajo UMS dedicado o un subproceso que no sea UMS.
-   UMS es más eficaz cuando la mayoría del procesamiento se realiza en modo de usuario. Siempre que sea posible, evite realizar llamadas del sistema en subprocesos de trabajo UMS.
-   Los subprocesos de trabajo ums no deben suponer que se está utilizando el programador del sistema. Esta suposición puede tener efectos sutiles; Por ejemplo, si un subproceso del código desconocido establece una prioridad o afinidad de subproceso, el programador UMS todavía podría invalidarlo. Es posible que el código que presupone que se está utilizando el programador del sistema no se comporte según lo previsto y se pueda interrumpir cuando lo llame un subproceso UMS.
-   Es posible que el sistema tenga que bloquear el contexto de subproceso de un subproceso de trabajo UMS. Por ejemplo, una llamada a procedimiento asincrónico en modo kernel (APC) podría cambiar el contexto del subproceso UMS, por lo que el contexto del subproceso debe estar bloqueado. Si el programador intenta ejecutar el contexto del subproceso UMS mientras está bloqueado, se producirá un error en la llamada. Este comportamiento es por diseño y el programador debe diseñarse para reintentar el acceso al contexto del subproceso UMS.

 

 
