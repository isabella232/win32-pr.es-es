---
title: Ejemplo de creación de un desencadenador inactivo
description: Para crear un desencadenador inactivo, debe especificar un desencadenador de inactividad al crear el desencadenador y debe establecer el tiempo de inactividad de la tarea. Para obtener información sobre las condiciones de inactividad, consulte condiciones de inactividad de tareas.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a7f8333c79d05dfade609f028f93a816e61adf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359237"
---
# <a name="creating-an-idle-trigger-example"></a><span data-ttu-id="09765-104">Ejemplo de creación de un desencadenador inactivo</span><span class="sxs-lookup"><span data-stu-id="09765-104">Creating an Idle Trigger Example</span></span>

<span data-ttu-id="09765-105">Para crear un desencadenador inactivo, debe especificar un desencadenador de inactividad al crear el desencadenador y debe establecer el tiempo de inactividad de la tarea.</span><span class="sxs-lookup"><span data-stu-id="09765-105">To create an idle trigger, you must specify an idle trigger when you create the trigger, and you must set the idle time for the task.</span></span> <span data-ttu-id="09765-106">Para obtener información sobre las condiciones de inactividad, consulte [condiciones de inactividad de tareas](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="09765-106">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

<span data-ttu-id="09765-107">Después de crear el desencadenador Idle, llame a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para guardar el nuevo desencadenador en el disco.</span><span class="sxs-lookup"><span data-stu-id="09765-107">After creating the idle trigger, call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to save the new trigger to disk.</span></span>

<span data-ttu-id="09765-108">En el procedimiento siguiente se describe cómo crear un desencadenador inactivo para una tarea conocida.</span><span class="sxs-lookup"><span data-stu-id="09765-108">The following procedure describes how to create an idle trigger for a known task.</span></span>

<span data-ttu-id="09765-109">**Para crear un desencadenador inactivo para una tarea conocida**</span><span class="sxs-lookup"><span data-stu-id="09765-109">**To create an idle trigger for a known task**</span></span>

1.  <span data-ttu-id="09765-110">Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="09765-110">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="09765-111">(En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).</span><span class="sxs-lookup"><span data-stu-id="09765-111">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="09765-112">Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea.</span><span class="sxs-lookup"><span data-stu-id="09765-112">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="09765-113">(Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").</span><span class="sxs-lookup"><span data-stu-id="09765-113">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="09765-114">Llame a [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) para establecer cuánto tiempo debe permanecer inactivo el sistema antes de que se active el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="09765-114">Call [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) to set how long the system must remain idle before the trigger will fire.</span></span> <span data-ttu-id="09765-115">(Tenga en cuenta que **SetIdleWait** se hereda de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)).</span><span class="sxs-lookup"><span data-stu-id="09765-115">(Note that **SetIdleWait** is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
4.  <span data-ttu-id="09765-116">Defina la estructura del [**\_ desencadenador**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) de la tarea y llame a [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para crear el desencadenador inactivo.</span><span class="sxs-lookup"><span data-stu-id="09765-116">Define the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure and call [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) to create the idle trigger.</span></span> <span data-ttu-id="09765-117">(Tenga en cuenta que **CreateTrigger** se hereda de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)).</span><span class="sxs-lookup"><span data-stu-id="09765-117">(Note that **CreateTrigger** is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
5.  <span data-ttu-id="09765-118">Guarde la tarea con el nuevo desencadenador de inactividad en el disco mediante [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="09765-118">Save the task with the new idle trigger to disk using [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="09765-119">(La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz com estándar compatible con la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) ).</span><span class="sxs-lookup"><span data-stu-id="09765-119">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
6.  <span data-ttu-id="09765-120">Llame a **ITask:: Release** para liberar todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="09765-120">Call **ITask::Release** to release all resources.</span></span> <span data-ttu-id="09765-121">(Tenga en cuenta que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) es un método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) heredado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).</span><span class="sxs-lookup"><span data-stu-id="09765-121">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="09765-122">Para obtener un ejemplo de código de</span><span class="sxs-lookup"><span data-stu-id="09765-122">For a code example of</span></span>                         | <span data-ttu-id="09765-123">Vea</span><span class="sxs-lookup"><span data-stu-id="09765-123">See</span></span>                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="09765-124">Crear un desencadenador inactivo para una tarea existente</span><span class="sxs-lookup"><span data-stu-id="09765-124">Creating an idle trigger for an existing task</span></span> | [<span data-ttu-id="09765-125">Ejemplo de código de C/C++: creación de un desencadenador inactivo</span><span class="sxs-lookup"><span data-stu-id="09765-125">C/C++ Code Example: Creating an Idle Trigger</span></span>](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a><span data-ttu-id="09765-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09765-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09765-127">Ejemplos de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="09765-127">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 