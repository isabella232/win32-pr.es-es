---
title: Ejemplo de finalización de una tarea
description: Puede finalizar una tarea mientras se está ejecutando mediante una llamada a IScheduledWorkItem Terminate.
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e632b00a9e957849a5735d31018e3444113190
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271316"
---
# <a name="terminating-a-task-example"></a><span data-ttu-id="6c675-103">Ejemplo de finalización de una tarea</span><span class="sxs-lookup"><span data-stu-id="6c675-103">Terminating a Task Example</span></span>

<span data-ttu-id="6c675-104">Puede finalizar una tarea mientras se está ejecutando mediante una llamada a [**IScheduledWorkItem:: Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).</span><span class="sxs-lookup"><span data-stu-id="6c675-104">You can terminate a task while it is running by calling [**IScheduledWorkItem::Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).</span></span>

<span data-ttu-id="6c675-105">En el procedimiento siguiente se describe cómo finalizar una tarea si se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="6c675-105">The following procedure describes how to terminate a task if it is running.</span></span>

<span data-ttu-id="6c675-106">**Para finalizar una tarea si se está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="6c675-106">**To terminate a task if it is running**</span></span>

1.  <span data-ttu-id="6c675-107">Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="6c675-107">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="6c675-108">(En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).</span><span class="sxs-lookup"><span data-stu-id="6c675-108">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="6c675-109">Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea.</span><span class="sxs-lookup"><span data-stu-id="6c675-109">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="6c675-110">(Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").</span><span class="sxs-lookup"><span data-stu-id="6c675-110">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="6c675-111">Llame a **ITask:: getStatus** para averiguar si la tarea se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="6c675-111">Call **ITask::GetStatus** to find out if the task is running.</span></span> <span data-ttu-id="6c675-112">(Tenga en cuenta que [**getStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) es un método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) heredado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).</span><span class="sxs-lookup"><span data-stu-id="6c675-112">(Note that [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
4.  <span data-ttu-id="6c675-113">Compruebe el estado de la tarea y, a continuación, llame a **ITask:: Terminate** si se está ejecutando la tarea.</span><span class="sxs-lookup"><span data-stu-id="6c675-113">Check the status of the task and then call **ITask::Terminate** if the task is running.</span></span> <span data-ttu-id="6c675-114">(Tenga en cuenta que [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) es un método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) heredado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).</span><span class="sxs-lookup"><span data-stu-id="6c675-114">(Note that [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="6c675-115">Para obtener un ejemplo de código de</span><span class="sxs-lookup"><span data-stu-id="6c675-115">For a code example of</span></span>                | <span data-ttu-id="6c675-116">Vea</span><span class="sxs-lookup"><span data-stu-id="6c675-116">See</span></span>                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6c675-117">Comprobar el estado de una tarea conocida</span><span class="sxs-lookup"><span data-stu-id="6c675-117">Verifying the status of a known task</span></span> | [<span data-ttu-id="6c675-118">Ejemplo de código de C/C++: finalizar una tarea</span><span class="sxs-lookup"><span data-stu-id="6c675-118">C/C++ Code Example: Terminating a Task</span></span>](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a><span data-ttu-id="6c675-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6c675-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c675-120">Ejemplos de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="6c675-120">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 