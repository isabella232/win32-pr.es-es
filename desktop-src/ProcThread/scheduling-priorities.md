---
description: Los subprocesos están programados para ejecutarse en función de su prioridad de programación.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Prioridades de programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e80c8baf4ed066ec7034c97850248f81c298c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677837"
---
# <a name="scheduling-priorities"></a><span data-ttu-id="c1b23-103">Prioridades de programación</span><span class="sxs-lookup"><span data-stu-id="c1b23-103">Scheduling Priorities</span></span>

<span data-ttu-id="c1b23-104">Los subprocesos están programados para ejecutarse en función de su *prioridad de programación*.</span><span class="sxs-lookup"><span data-stu-id="c1b23-104">Threads are scheduled to run based on their *scheduling priority*.</span></span> <span data-ttu-id="c1b23-105">A cada subproceso se le asigna una prioridad de programación.</span><span class="sxs-lookup"><span data-stu-id="c1b23-105">Each thread is assigned a scheduling priority.</span></span> <span data-ttu-id="c1b23-106">Los niveles de prioridad van desde cero (prioridad más baja) hasta 31 (prioridad más alta).</span><span class="sxs-lookup"><span data-stu-id="c1b23-106">The priority levels range from zero (lowest priority) to 31 (highest priority).</span></span> <span data-ttu-id="c1b23-107">Solo el subproceso de página cero puede tener una prioridad de cero.</span><span class="sxs-lookup"><span data-stu-id="c1b23-107">Only the zero-page thread can have a priority of zero.</span></span> <span data-ttu-id="c1b23-108">(El subproceso de página cero es un subproceso del sistema responsable de cero páginas libres cuando no hay otros subprocesos que deban ejecutarse).</span><span class="sxs-lookup"><span data-stu-id="c1b23-108">(The zero-page thread is a system thread responsible for zeroing any free pages when there are no other threads that need to run.)</span></span>

<span data-ttu-id="c1b23-109">El sistema trata todos los subprocesos con la misma prioridad que iguales.</span><span class="sxs-lookup"><span data-stu-id="c1b23-109">The system treats all threads with the same priority as equal.</span></span> <span data-ttu-id="c1b23-110">El sistema asigna los intervalos de tiempo en un modo Round-Robin a todos los subprocesos con la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="c1b23-110">The system assigns time slices in a round-robin fashion to all threads with the highest priority.</span></span> <span data-ttu-id="c1b23-111">Si ninguno de estos subprocesos está listo para ejecutarse, el sistema asigna los intervalos de tiempo en un modo Round-Robin a todos los subprocesos con la siguiente prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="c1b23-111">If none of these threads are ready to run, the system assigns time slices in a round-robin fashion to all threads with the next highest priority.</span></span> <span data-ttu-id="c1b23-112">Si un subproceso de mayor prioridad está disponible para ejecutarse, el sistema deja de ejecutar el subproceso de prioridad más baja (sin permitir que termine de usar su intervalo de tiempo) y asigna un intervalo de tiempo completo al subproceso de prioridad superior.</span><span class="sxs-lookup"><span data-stu-id="c1b23-112">If a higher-priority thread becomes available to run, the system ceases to execute the lower-priority thread (without allowing it to finish using its time slice) and assigns a full time slice to the higher-priority thread.</span></span> <span data-ttu-id="c1b23-113">Para obtener más información, vea [cambios de contexto](context-switches.md).</span><span class="sxs-lookup"><span data-stu-id="c1b23-113">For more information, see [Context Switches](context-switches.md).</span></span>

<span data-ttu-id="c1b23-114">La prioridad de cada subproceso viene determinada por los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="c1b23-114">The priority of each thread is determined by the following criteria:</span></span>

-   <span data-ttu-id="c1b23-115">La clase de prioridad de su proceso</span><span class="sxs-lookup"><span data-stu-id="c1b23-115">The priority class of its process</span></span>
-   <span data-ttu-id="c1b23-116">Nivel de prioridad del subproceso dentro de la clase de prioridad de su proceso.</span><span class="sxs-lookup"><span data-stu-id="c1b23-116">The priority level of the thread within the priority class of its process</span></span>

<span data-ttu-id="c1b23-117">La clase de prioridad y el nivel de prioridad se combinan para formar la *prioridad base* de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="c1b23-117">The priority class and priority level are combined to form the *base priority* of a thread.</span></span> <span data-ttu-id="c1b23-118">Para obtener información sobre la prioridad dinámica de un subproceso, consulte [aumentos de prioridad](priority-boosts.md).</span><span class="sxs-lookup"><span data-stu-id="c1b23-118">For information on the dynamic priority of a thread, see [Priority Boosts](priority-boosts.md).</span></span>

## <a name="priority-class"></a><span data-ttu-id="c1b23-119">Priority (clase)</span><span class="sxs-lookup"><span data-stu-id="c1b23-119">Priority Class</span></span>

<span data-ttu-id="c1b23-120">Cada proceso pertenece a una de las siguientes clases de prioridad:</span><span class="sxs-lookup"><span data-stu-id="c1b23-120">Each process belongs to one of the following priority classes:</span></span><dl> <span data-ttu-id="c1b23-121">\_clase de prioridad INactiva \_</span><span class="sxs-lookup"><span data-stu-id="c1b23-121">IDLE\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="c1b23-122">POR debajo de la \_ \_ clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="c1b23-122">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="c1b23-123">\_clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="c1b23-123">NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="c1b23-124">POR encima de la \_ \_ clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="c1b23-124">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="c1b23-125">\_clase de prioridad alta \_</span><span class="sxs-lookup"><span data-stu-id="c1b23-125">HIGH\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="c1b23-126">\_clase de prioridad en tiempo real \_</span><span class="sxs-lookup"><span data-stu-id="c1b23-126">REALTIME\_PRIORITY\_CLASS</span></span>  
</dl>

<span data-ttu-id="c1b23-127">De forma predeterminada, la clase de prioridad de un proceso es la \_ clase de prioridad normal \_ .</span><span class="sxs-lookup"><span data-stu-id="c1b23-127">By default, the priority class of a process is NORMAL\_PRIORITY\_CLASS.</span></span> <span data-ttu-id="c1b23-128">Utilice la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) para especificar la clase de prioridad de un proceso secundario cuando lo cree.</span><span class="sxs-lookup"><span data-stu-id="c1b23-128">Use the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function to specify the priority class of a child process when you create it.</span></span> <span data-ttu-id="c1b23-129">Si el proceso que realiza la llamada es una clase de prioridad inactiva \_ o una \_ clase de \_ \_ prioridad normal \_ , el nuevo proceso heredará esta clase.</span><span class="sxs-lookup"><span data-stu-id="c1b23-129">If the calling process is IDLE\_PRIORITY\_CLASS or BELOW\_NORMAL\_PRIORITY\_CLASS, the new process will inherit this class.</span></span> <span data-ttu-id="c1b23-130">Utilice la función [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) para determinar la clase de prioridad actual de un proceso y la función [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) para cambiar la clase de prioridad de un proceso.</span><span class="sxs-lookup"><span data-stu-id="c1b23-130">Use the [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) function to determine the current priority class of a process and the [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) function to change the priority class of a process.</span></span>

<span data-ttu-id="c1b23-131">Los procesos que supervisan el sistema, como los protectores de pantalla o las aplicaciones que actualizan periódicamente una pantalla, deben usar la clase de prioridad inactiva \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c1b23-131">Processes that monitor the system, such as screen savers or applications that periodically update a display, should use IDLE\_PRIORITY\_CLASS.</span></span> <span data-ttu-id="c1b23-132">Esto evita que los subprocesos de este proceso, que no tienen una prioridad alta, interfieran con subprocesos de mayor prioridad.</span><span class="sxs-lookup"><span data-stu-id="c1b23-132">This prevents the threads of this process, which do not have high priority, from interfering with higher priority threads.</span></span>

<span data-ttu-id="c1b23-133">Use la \_ \_ clase de prioridad alta con cuidado.</span><span class="sxs-lookup"><span data-stu-id="c1b23-133">Use HIGH\_PRIORITY\_CLASS with care.</span></span> <span data-ttu-id="c1b23-134">Si un subproceso se ejecuta en el nivel de prioridad más alto durante períodos prolongados, otros subprocesos del sistema no obtendrán el tiempo de procesador.</span><span class="sxs-lookup"><span data-stu-id="c1b23-134">If a thread runs at the highest priority level for extended periods, other threads in the system will not get processor time.</span></span> <span data-ttu-id="c1b23-135">Si varios subprocesos se establecen en alta prioridad al mismo tiempo, los subprocesos pierden su eficacia.</span><span class="sxs-lookup"><span data-stu-id="c1b23-135">If several threads are set at high priority at the same time, the threads lose their effectiveness.</span></span> <span data-ttu-id="c1b23-136">La clase de prioridad alta se debe reservar para los subprocesos que deben responder a eventos críticos en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c1b23-136">The high-priority class should be reserved for threads that must respond to time-critical events.</span></span> <span data-ttu-id="c1b23-137">Si la aplicación realiza una tarea que requiere la clase de prioridad alta, mientras que el resto de sus tareas es una prioridad normal, use [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) para aumentar temporalmente la clase de prioridad de la aplicación. a continuación, reduzca el tiempo después de que se haya completado la tarea crítica temporal.</span><span class="sxs-lookup"><span data-stu-id="c1b23-137">If your application performs one task that requires the high-priority class while the rest of its tasks are normal priority, use [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) to raise the priority class of the application temporarily; then reduce it after the time-critical task has been completed.</span></span> <span data-ttu-id="c1b23-138">Otra estrategia consiste en crear un proceso de alta prioridad que tenga todos los subprocesos bloqueados la mayor parte del tiempo, activando los subprocesos solo cuando se necesitan tareas críticas.</span><span class="sxs-lookup"><span data-stu-id="c1b23-138">Another strategy is to create a high-priority process that has all of its threads blocked most of the time, awakening threads only when critical tasks are needed.</span></span> <span data-ttu-id="c1b23-139">Lo importante es que un subproceso de prioridad alta debe ejecutarse durante un breve período de tiempo y solo cuando tenga trabajo crítico en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c1b23-139">The important point is that a high-priority thread should execute for a brief time, and only when it has time-critical work to perform.</span></span>

<span data-ttu-id="c1b23-140">Casi nunca se debe usar \_ \_ la clase de prioridad en tiempo real, porque interrumpe los subprocesos del sistema que administran la entrada del mouse, la entrada del teclado y el vaciado del disco en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="c1b23-140">You should almost never use REALTIME\_PRIORITY\_CLASS, because this interrupts system threads that manage mouse input, keyboard input, and background disk flushing.</span></span> <span data-ttu-id="c1b23-141">Esta clase puede ser adecuada para las aplicaciones que "hablan" directamente en el hardware o que realizan tareas breves que deben tener interrupciones limitadas.</span><span class="sxs-lookup"><span data-stu-id="c1b23-141">This class can be appropriate for applications that "talk" directly to hardware or that perform brief tasks that should have limited interruptions.</span></span>

## <a name="priority-level"></a><span data-ttu-id="c1b23-142">Nivel de prioridad</span><span class="sxs-lookup"><span data-stu-id="c1b23-142">Priority Level</span></span>

<span data-ttu-id="c1b23-143">A continuación se muestran los niveles de prioridad dentro de cada clase de prioridad:</span><span class="sxs-lookup"><span data-stu-id="c1b23-143">The following are priority levels within each priority class:</span></span><dl> <span data-ttu-id="c1b23-144">prioridad de subproceso \_ \_ inactiva</span><span class="sxs-lookup"><span data-stu-id="c1b23-144">THREAD\_PRIORITY\_IDLE</span></span>  
<span data-ttu-id="c1b23-145">prioridad de subproceso \_ \_ más baja</span><span class="sxs-lookup"><span data-stu-id="c1b23-145">THREAD\_PRIORITY\_LOWEST</span></span>  
<span data-ttu-id="c1b23-146">prioridad de subproceso \_ \_ por debajo de lo \_ normal</span><span class="sxs-lookup"><span data-stu-id="c1b23-146">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  
<span data-ttu-id="c1b23-147">prioridad de subproceso \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="c1b23-147">THREAD\_PRIORITY\_NORMAL</span></span>  
<span data-ttu-id="c1b23-148">prioridad de subproceso \_ \_ por encima de lo \_ normal</span><span class="sxs-lookup"><span data-stu-id="c1b23-148">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  
<span data-ttu-id="c1b23-149">prioridad de subproceso \_ \_ más alta</span><span class="sxs-lookup"><span data-stu-id="c1b23-149">THREAD\_PRIORITY\_HIGHEST</span></span>  
<span data-ttu-id="c1b23-150">tiempo de prioridad de subproceso \_ \_ \_ crítico</span><span class="sxs-lookup"><span data-stu-id="c1b23-150">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span>  
</dl>

<span data-ttu-id="c1b23-151">Todos los subprocesos se crean mediante la prioridad de subproceso \_ \_ normal.</span><span class="sxs-lookup"><span data-stu-id="c1b23-151">All threads are created using THREAD\_PRIORITY\_NORMAL.</span></span> <span data-ttu-id="c1b23-152">Esto significa que la prioridad del subproceso es la misma que la clase de prioridad del proceso.</span><span class="sxs-lookup"><span data-stu-id="c1b23-152">This means that the thread priority is the same as the process priority class.</span></span> <span data-ttu-id="c1b23-153">Después de crear un subproceso, utilice la función [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) para ajustar su prioridad en relación con otros subprocesos del proceso.</span><span class="sxs-lookup"><span data-stu-id="c1b23-153">After you create a thread, use the [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) function to adjust its priority relative to other threads in the process.</span></span>

<span data-ttu-id="c1b23-154">Una estrategia típica es usar la prioridad de subprocesos por \_ \_ encima \_ \_ de la normal o la prioridad de subproceso \_ más alta para el subproceso de entrada del proceso, para asegurarse de que la aplicación responde al usuario.</span><span class="sxs-lookup"><span data-stu-id="c1b23-154">A typical strategy is to use THREAD\_PRIORITY\_ABOVE\_NORMAL or THREAD\_PRIORITY\_HIGHEST for the process's input thread, to ensure that the application is responsive to the user.</span></span> <span data-ttu-id="c1b23-155">Los subprocesos en segundo plano, especialmente aquellos que usan un uso intensivo del procesador, se pueden establecer en prioridad de subproceso \_ \_ por debajo de la \_ prioridad normal o de subproceso \_ \_ más baja, para asegurarse de que se pueden cambiar cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="c1b23-155">Background threads, particularly those that are processor intensive, can be set to THREAD\_PRIORITY\_BELOW\_NORMAL or THREAD\_PRIORITY\_LOWEST, to ensure that they can be preempted when necessary.</span></span> <span data-ttu-id="c1b23-156">Sin embargo, si tiene un subproceso que está esperando a otro subproceso con una prioridad más baja para completar alguna tarea, asegúrese de bloquear la ejecución del subproceso de alta prioridad en espera.</span><span class="sxs-lookup"><span data-stu-id="c1b23-156">However, if you have a thread waiting for another thread with a lower priority to complete some task, be sure to block the execution of the waiting high-priority thread.</span></span> <span data-ttu-id="c1b23-157">Para ello, use una [función wait](../sync/wait-functions.md), una [sección Critical](../sync/critical-section-objects.md)o la función [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) , [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)o [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) .</span><span class="sxs-lookup"><span data-stu-id="c1b23-157">To do this, use a [wait function](../sync/wait-functions.md), [critical section](../sync/critical-section-objects.md), or the [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) function, [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), or [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) function.</span></span> <span data-ttu-id="c1b23-158">Es preferible que el subproceso ejecute un bucle.</span><span class="sxs-lookup"><span data-stu-id="c1b23-158">This is preferable to having the thread execute a loop.</span></span> <span data-ttu-id="c1b23-159">De lo contrario, el proceso puede quedar interbloqueado, ya que el subproceso con prioridad inferior nunca está programado.</span><span class="sxs-lookup"><span data-stu-id="c1b23-159">Otherwise, the process may become deadlocked, because the thread with lower priority is never scheduled.</span></span>

<span data-ttu-id="c1b23-160">Para determinar el nivel de prioridad actual de un subproceso, utilice la función [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) .</span><span class="sxs-lookup"><span data-stu-id="c1b23-160">To determine the current priority level of a thread, use the [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) function.</span></span>

## <a name="base-priority"></a><span data-ttu-id="c1b23-161">Prioridad base</span><span class="sxs-lookup"><span data-stu-id="c1b23-161">Base Priority</span></span>

<span data-ttu-id="c1b23-162">La clase de prioridad del proceso y el nivel de prioridad del subproceso se combinan para formar la prioridad base de cada subproceso.</span><span class="sxs-lookup"><span data-stu-id="c1b23-162">The process priority class and thread priority level are combined to form the base priority of each thread.</span></span>

<span data-ttu-id="c1b23-163">En la tabla siguiente se muestra la prioridad base de las combinaciones de clase de prioridad de proceso y valor de prioridad de subproceso.</span><span class="sxs-lookup"><span data-stu-id="c1b23-163">The following table shows the base priority for combinations of process priority class and thread priority value.</span></span>


<table>
<tr>
<th colspan="2"><span data-ttu-id="c1b23-164">Clase de prioridad del proceso</span><span class="sxs-lookup"><span data-stu-id="c1b23-164">Process priority class</span></span></th>
<th><span data-ttu-id="c1b23-165">Nivel de prioridad de subproceso</span><span class="sxs-lookup"><span data-stu-id="c1b23-165">Thread priority level</span></span></th>
<th><span data-ttu-id="c1b23-166">Prioridad base</span><span class="sxs-lookup"><span data-stu-id="c1b23-166">Base priority</span></span></th>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="c1b23-167">IDLE_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="c1b23-167">IDLE_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="c1b23-168">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="c1b23-168">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="c1b23-169">1</span><span class="sxs-lookup"><span data-stu-id="c1b23-169">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-170">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="c1b23-170">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="c1b23-171">2</span><span class="sxs-lookup"><span data-stu-id="c1b23-171">2</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-172">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-172">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-173">3</span><span class="sxs-lookup"><span data-stu-id="c1b23-173">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-174">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-174">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-175">4</span><span class="sxs-lookup"><span data-stu-id="c1b23-175">4</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-176">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-176">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-177">5</span><span class="sxs-lookup"><span data-stu-id="c1b23-177">5</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-178">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="c1b23-178">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="c1b23-179">6</span><span class="sxs-lookup"><span data-stu-id="c1b23-179">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-180">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-180">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="c1b23-181">15</span><span class="sxs-lookup"><span data-stu-id="c1b23-181">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="c1b23-182">BELOW_NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="c1b23-182">BELOW_NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="c1b23-183">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="c1b23-183">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="c1b23-184">1</span><span class="sxs-lookup"><span data-stu-id="c1b23-184">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-185">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="c1b23-185">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="c1b23-186">4</span><span class="sxs-lookup"><span data-stu-id="c1b23-186">4</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-187">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-187">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-188">5</span><span class="sxs-lookup"><span data-stu-id="c1b23-188">5</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-189">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-189">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-190">6</span><span class="sxs-lookup"><span data-stu-id="c1b23-190">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-191">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-191">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-192">7</span><span class="sxs-lookup"><span data-stu-id="c1b23-192">7</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-193">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="c1b23-193">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="c1b23-194">8</span><span class="sxs-lookup"><span data-stu-id="c1b23-194">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-195">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-195">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="c1b23-196">15</span><span class="sxs-lookup"><span data-stu-id="c1b23-196">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="c1b23-197">NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="c1b23-197">NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="c1b23-198">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="c1b23-198">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="c1b23-199">1</span><span class="sxs-lookup"><span data-stu-id="c1b23-199">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-200">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="c1b23-200">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="c1b23-201">6</span><span class="sxs-lookup"><span data-stu-id="c1b23-201">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-202">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-202">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-203">7</span><span class="sxs-lookup"><span data-stu-id="c1b23-203">7</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-204">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-204">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-205">8</span><span class="sxs-lookup"><span data-stu-id="c1b23-205">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-206">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-206">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-207">9</span><span class="sxs-lookup"><span data-stu-id="c1b23-207">9</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-208">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="c1b23-208">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="c1b23-209">10</span><span class="sxs-lookup"><span data-stu-id="c1b23-209">10</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-210">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-210">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="c1b23-211">15</span><span class="sxs-lookup"><span data-stu-id="c1b23-211">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="c1b23-212">ABOVE_NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="c1b23-212">ABOVE_NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="c1b23-213">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="c1b23-213">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="c1b23-214">1</span><span class="sxs-lookup"><span data-stu-id="c1b23-214">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-215">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="c1b23-215">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="c1b23-216">8</span><span class="sxs-lookup"><span data-stu-id="c1b23-216">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-217">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-217">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-218">9</span><span class="sxs-lookup"><span data-stu-id="c1b23-218">9</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-219">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-219">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-220">10</span><span class="sxs-lookup"><span data-stu-id="c1b23-220">10</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-221">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-221">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-222">11</span><span class="sxs-lookup"><span data-stu-id="c1b23-222">11</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-223">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="c1b23-223">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="c1b23-224">12</span><span class="sxs-lookup"><span data-stu-id="c1b23-224">12</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-225">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-225">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="c1b23-226">15</span><span class="sxs-lookup"><span data-stu-id="c1b23-226">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="c1b23-227">HIGH_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="c1b23-227">HIGH_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="c1b23-228">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="c1b23-228">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="c1b23-229">1</span><span class="sxs-lookup"><span data-stu-id="c1b23-229">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-230">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="c1b23-230">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="c1b23-231">11</span><span class="sxs-lookup"><span data-stu-id="c1b23-231">11</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-232">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-232">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-233">12</span><span class="sxs-lookup"><span data-stu-id="c1b23-233">12</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-234">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-234">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-235">13</span><span class="sxs-lookup"><span data-stu-id="c1b23-235">13</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-236">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-236">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-237">14</span><span class="sxs-lookup"><span data-stu-id="c1b23-237">14</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-238">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="c1b23-238">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="c1b23-239">15</span><span class="sxs-lookup"><span data-stu-id="c1b23-239">15</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-240">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-240">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="c1b23-241">15</span><span class="sxs-lookup"><span data-stu-id="c1b23-241">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="c1b23-242">REALTIME_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="c1b23-242">REALTIME_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="c1b23-243">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="c1b23-243">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="c1b23-244">16</span><span class="sxs-lookup"><span data-stu-id="c1b23-244">16</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-245">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="c1b23-245">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="c1b23-246">22</span><span class="sxs-lookup"><span data-stu-id="c1b23-246">22</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-247">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-247">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-248">23</span><span class="sxs-lookup"><span data-stu-id="c1b23-248">23</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-249">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-249">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-250">24</span><span class="sxs-lookup"><span data-stu-id="c1b23-250">24</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-251">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-251">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="c1b23-252">25</span><span class="sxs-lookup"><span data-stu-id="c1b23-252">25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-253">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="c1b23-253">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="c1b23-254">26</span><span class="sxs-lookup"><span data-stu-id="c1b23-254">26</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1b23-255">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="c1b23-255">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="c1b23-256">31</span><span class="sxs-lookup"><span data-stu-id="c1b23-256">31</span></span></td>
</tr>
</table>

 

 

 
