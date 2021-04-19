---
description: La programación de modo de usuario (UMS) es un mecanismo ligero que las aplicaciones pueden usar para programar sus propios subprocesos.
ms.assetid: f9dd92fe-6d7a-452c-893e-e6df1757e377
title: Programación de User-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ceea3c4d4e40d73f48414d074bcb5b4f6e911d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677984"
---
# <a name="user-mode-scheduling"></a>Programación de User-Mode

La programación de modo de usuario (UMS) es un mecanismo ligero que las aplicaciones pueden usar para programar sus propios subprocesos. Una aplicación puede cambiar entre los subprocesos UMS en modo de usuario sin que intervenga el [programador del sistema](scheduling.md) y recuperar el control del procesador si un SUBproceso UMS se bloquea en el kernel. Los subprocesos UMS se diferencian de las [fibras](fibers.md) en que cada subproceso UMS tiene su propio contexto de subproceso en lugar de compartir el contexto del subproceso de un solo subproceso. La capacidad de cambiar entre subprocesos en modo de usuario hace que UMS sea más eficaz que los [grupos de subprocesos](thread-pools.md) para administrar un gran número de elementos de trabajo de corta duración que requieren pocas llamadas del sistema.

UMS se recomienda para las aplicaciones con requisitos de alto rendimiento que necesitan ejecutar de forma eficaz muchos subprocesos simultáneamente en sistemas multiprocesador o de varios núcleos. Para aprovechar las ventajas de UMS, una aplicación debe implementar un componente de programador que administre los subprocesos UMS de la aplicación y determine Cuándo deben ejecutarse. Los desarrolladores deben considerar si sus requisitos de rendimiento de la aplicación justifican el trabajo implicado en el desarrollo de este componente. Es posible que las aplicaciones con requisitos de rendimiento moderados se puedan atender mejor permitiendo que el programador del sistema Programe sus subprocesos.

UMS está disponible para las aplicaciones de 64 bits que se ejecutan en versiones de 64 bits de Windows 7 y Windows Server 2008 R2 o versiones posteriores de 64 bits de Windows. Esta característica no está disponible en las versiones de 32 bits de Windows.

Para obtener más información, consulte las siguientes secciones:

-   [Programador UMS](#ums-scheduler)
-   [Subproceso del programador UMS](#ums-scheduler-thread)
-   [Subprocesos de trabajo UMS, contextos de subproceso y listas de finalización](#ums-worker-threads-thread-contexts-and-completion-lists)
-   [Función de punto de entrada del programador UMS](#ums-scheduler-entry-point-function)
-   [Ejecución del subproceso UMS](#ums-thread-execution)
-   [Prácticas recomendadas de UMS](#ums-best-practices)

## <a name="ums-scheduler"></a>Programador UMS

El programador UMS de una aplicación es responsable de crear, administrar y eliminar los subprocesos UMS y determinar qué subproceso UMS ejecutar. El programador de una aplicación realiza las siguientes tareas:

-   Crea un subproceso de programador UMS para cada procesador en el que la aplicación ejecutará los subprocesos de trabajo UMS.
-   Crea subprocesos de trabajo UMS para realizar el trabajo de la aplicación.
-   Mantiene su propia cola de subprocesos preparada de subprocesos de trabajo listos para ejecutarse y selecciona los subprocesos que se ejecutan en función de las directivas de programación de la aplicación.
-   Crea y supervisa una o varias listas de finalización en las que el sistema pone en cola los subprocesos después de finalizar el procesamiento en el kernel. Entre estos se incluyen los subprocesos de trabajo y subprocesos recién creados bloqueados previamente en una llamada del sistema que se han desbloqueado.
-   Proporciona una función de punto de entrada del programador para controlar las notificaciones del sistema. El sistema llama a la función de punto de entrada cuando se crea un subproceso de programador, cuando un subproceso de trabajo se bloquea en una llamada del sistema o cuando un subproceso de trabajo cede explícitamente el control.
-   Realiza tareas de limpieza para los subprocesos de trabajo que han terminado de ejecutarse.
-   Realiza un cierre ordenado del programador cuando lo solicita la aplicación.

## <a name="ums-scheduler-thread"></a>Subproceso del programador UMS

Un subproceso de programador UMS es un subproceso normal que se ha convertido en UMS mediante una llamada a la función [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) . El programador del sistema determina cuándo se ejecuta el subproceso del programador UMS en función de su prioridad en relación con otros subprocesos listos. El procesador en el que se ejecuta el subproceso del programador se ve afectado por la afinidad del subproceso, igual que para los subprocesos que no son UMS.

El autor de la llamada de [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) especifica una lista de finalización y una función de punto de entrada [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) que se va a asociar al subproceso del programador UMS. El sistema llama a la función de punto de entrada especificada cuando ha terminado de convertir el subproceso que realiza la llamada a UMS. La función de punto de entrada del programador es responsable de determinar la siguiente acción adecuada para el subproceso especificado. Para obtener más información, vea [función de punto de entrada del programador UMS](#ums-scheduler-entry-point-function) más adelante en este tema.

Una aplicación puede crear un subproceso de programador UMS para cada procesador que se usará para ejecutar subprocesos UMS. La aplicación también podría establecer la afinidad de cada subproceso del programador UMS para un procesador lógico específico, lo que tiende a excluir subprocesos no relacionados que se ejecutan en ese procesador y que, de hecho, lo reservan para ese subproceso del programador. Tenga en cuenta que establecer la afinidad de subprocesos de este modo puede afectar al rendimiento global del sistema al privar a otros procesos que se puedan estar ejecutando en el sistema. Para obtener más información acerca de la afinidad de subprocesos, vea [varios procesadores](multiple-processors.md).

## <a name="ums-worker-threads-thread-contexts-and-completion-lists"></a>Subprocesos de trabajo UMS, contextos de subproceso y listas de finalización

Un subproceso de trabajo UMS se crea mediante una llamada a [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) con el atributo de subproceso de procedimiento \_ \_ \_ UMS \_ y especifica un contexto de subproceso UMS y una lista de finalización.

Un contexto de subproceso UMS representa el estado de subproceso UMS de un subproceso de trabajo y se usa para identificar el subproceso de trabajo en las llamadas a funciones UMS. Se crea llamando a [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext).

Una lista de finalización se crea mediante una llamada a la función [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist) . Una lista de finalización recibe los subprocesos de trabajo de UMS que han completado la ejecución en el kernel y están listos para ejecutarse en modo de usuario. Solo el sistema puede poner en cola los subprocesos de trabajo en una lista de finalización. Los nuevos subprocesos de trabajo UMS se ponen en cola automáticamente en la lista de finalización especificada cuando se crearon los subprocesos. Los subprocesos de trabajo previamente bloqueados también se ponen en cola en la lista de finalización cuando ya no se bloquean.

Cada subproceso del programador UMS está asociado a una sola lista de finalización. Sin embargo, la misma lista de finalización se puede asociar a cualquier número de subprocesos del programador UMS y un subproceso del programador puede recuperar contextos UMS de cualquier lista de finalización para la que tenga un puntero.

Cada lista de finalización tiene un evento asociado que el sistema señala cuando pone en cola uno o más subprocesos de trabajo en una lista vacía. La función [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent) recupera un identificador para el evento para una lista de finalización especificada. Una aplicación puede esperar en más de un evento de lista de finalización junto con otros eventos que tienen sentido para la aplicación.

## <a name="ums-scheduler-entry-point-function"></a>Función de punto de entrada del programador UMS

La función de punto de entrada del programador de una aplicación se implementa como una función [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) . El sistema llama a la función de punto de entrada del programador de la aplicación en las siguientes ocasiones:

-   Cuando un subproceso que no es UMS se convierte en un subproceso del programador UMS llamando a [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode).
-   Cuando un subproceso de trabajo UMS llama a [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield).
-   Cuando un subproceso de trabajo UMS se bloquea en un servicio del sistema, como una llamada del sistema o un error de página.

El parámetro *Reason* de la función [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) especifica la razón por la que se llamó a la función de punto de entrada. Si se llamó a la función de punto de entrada porque se creó un nuevo subproceso de programador UMS, el parámetro *SchedulerParam* contiene los datos especificados por el autor de la llamada de [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode). Si se llamó a la función de punto de entrada porque se produjo un subproceso de trabajo UMS, el parámetro *SchedulerParam* contiene los datos especificados por el autor de la llamada de [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield). Si se llamó a la función de punto de entrada porque un subproceso de trabajo UMS se bloqueó en el kernel, el parámetro *SchedulerParam* es NULL.

La función de punto de entrada del programador es responsable de determinar la siguiente acción adecuada para el subproceso especificado. Por ejemplo, si se bloquea un subproceso de trabajo, la función de punto de entrada del programador podría ejecutar el siguiente subproceso de trabajo UMS listo y disponible.

Cuando se llama a la función de punto de entrada del programador, el programador de la aplicación debe intentar recuperar todos los elementos de la lista de finalización asociada llamando a la función [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) . Esta función recupera una lista de contextos de subprocesos UMS que han terminado de procesarse en el kernel y están listos para ejecutarse en modo de usuario. El programador de la aplicación no debe ejecutar los subprocesos UMS directamente desde esta lista, ya que esto puede provocar un comportamiento imprevisible en la aplicación. En su lugar, el programador debe recuperar todos los contextos de subprocesos UMS llamando a la función [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem) una vez para cada contexto, inserte los contextos de subproceso UMS en la cola de subprocesos preparada del programador y, a continuación, ejecute únicamente los subprocesos UMS desde la cola de subprocesos listos.

Si el programador no necesita esperar en varios eventos, debe llamar a [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) con un parámetro de tiempo de espera distinto de cero para que la función espere en el evento de lista de finalización antes de devolver. Si el programador necesita esperar en varios eventos de lista de finalización, debe llamar a **DequeueUmsCompletionListItems** con un parámetro de tiempo de espera de cero para que la función se devuelva inmediatamente, incluso si la lista de finalización está vacía. En este caso, el programador puede esperar explícitamente los eventos de la lista de finalización, por ejemplo, mediante [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects).

## <a name="ums-thread-execution"></a>Ejecución del subproceso UMS

Un subproceso de trabajo UMS recién creado se pone en la cola de la lista de finalización especificada y no comienza a ejecutarse hasta que el programador UMS de la aplicación lo selecciona para ejecutarse. Esto difiere de los subprocesos que no son UMS, que el programador de sistema programa automáticamente para ejecutarse, a menos que el llamador cree explícitamente el subproceso suspendido.

Scheduler ejecuta un subproceso de trabajo mediante una llamada a [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread) con el contexto UMS del subproceso de trabajo. Un subproceso de trabajo UMS se ejecuta hasta que produce una llamada a la función [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield) , bloques o finaliza.

## <a name="ums-best-practices"></a>Prácticas recomendadas de UMS

Las aplicaciones que implementan UMS deben seguir estos procedimientos recomendados:

-   El sistema administra las estructuras subyacentes para los contextos de subprocesos UMS y no se debe modificar directamente. En su lugar, use [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation) y [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation) para recuperar y establecer información acerca de un subproceso de trabajo UMS.
-   Para ayudar a evitar los interbloqueos, el subproceso del programador UMS no debe compartir bloqueos con subprocesos de trabajo UMS. Esto incluye tanto los bloqueos creados por la aplicación como los bloqueos del sistema adquiridos indirectamente por operaciones como la asignación del montón o la carga de archivos dll. Por ejemplo, supongamos que Scheduler ejecuta un subproceso de trabajo UMS que carga un archivo DLL. El subproceso de trabajo adquiere el bloqueo y los bloques del cargador. El sistema llama a la función de punto de entrada del programador, que luego carga un archivo DLL. Esto provoca un interbloqueo, porque el bloqueo del cargador ya se mantiene y no se puede liberar hasta que el primer subproceso se desbloquea. Para evitar este problema, delegue el trabajo que podría compartir bloqueos con subprocesos de trabajo UMS en un subproceso de trabajo UMS dedicado o en un subproceso no UMS.
-   UMS es más eficaz cuando la mayor parte del procesamiento se realiza en modo de usuario. Siempre que sea posible, Evite realizar llamadas del sistema en subprocesos de trabajo UMS.
-   Los subprocesos de trabajo UMS no deben asumir que se está usando el programador del sistema. Esta suposición puede tener efectos sutiles; por ejemplo, si un subproceso en el código desconocido establece una prioridad o afinidad de subprocesos, el programador UMS podría reemplazarlo. Es posible que el código que supone el uso del programador del sistema no se comporte de la manera esperada y que se interrumpa cuando lo llame un subproceso UMS.
-   Es posible que el sistema tenga que bloquear el contexto del subproceso de un subproceso de trabajo UMS. Por ejemplo, una llamada a procedimiento asincrónico (APC) en modo kernel podría cambiar el contexto del subproceso UMS, por lo que el contexto del subproceso debe estar bloqueado. Si Scheduler intenta ejecutar el contexto del subproceso UMS mientras está bloqueado, se producirá un error en la llamada. Este comportamiento es así por diseño y el programador debe estar diseñado para reintentar el acceso al contexto del subproceso UMS.

 

 
