---
title: Crear un nuevo desencadenador
description: Para crear un desencadenador, debe usar tres interfaces.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48ecb7b06e5bade6d5ad80e4c9a82794f6a17e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421076"
---
# <a name="creating-a-new-trigger"></a><span data-ttu-id="b52de-103">Crear un nuevo desencadenador</span><span class="sxs-lookup"><span data-stu-id="b52de-103">Creating a New Trigger</span></span>

<span data-ttu-id="b52de-104">Para crear un desencadenador, debe usar tres interfaces.</span><span class="sxs-lookup"><span data-stu-id="b52de-104">To create a trigger you must use three interfaces.</span></span> <span data-ttu-id="b52de-105">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) proporciona el método [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para crear el objeto de desencadenador, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) proporciona el método [**ITaskTrigger:: SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) para establecer los criterios del desencadenador y la interfaz com [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) proporciona un método para **Guardar** el nuevo desencadenador en el disco.</span><span class="sxs-lookup"><span data-stu-id="b52de-105">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) provides the [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) method for creating the trigger object, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) provides the [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) method for setting the criteria for the trigger, and the COM interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) provides a **Save** method for saving the new trigger to disk.</span></span>

<span data-ttu-id="b52de-106">En el procedimiento siguiente se describe cómo crear un nuevo desencadenador.</span><span class="sxs-lookup"><span data-stu-id="b52de-106">The following procedure describes how to create a new trigger.</span></span>

<span data-ttu-id="b52de-107">**Para crear un nuevo desencadenador**</span><span class="sxs-lookup"><span data-stu-id="b52de-107">**To create a new trigger**</span></span>

1.  <span data-ttu-id="b52de-108">Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="b52de-108">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="b52de-109">(En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).</span><span class="sxs-lookup"><span data-stu-id="b52de-109">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="b52de-110">Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea.</span><span class="sxs-lookup"><span data-stu-id="b52de-110">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="b52de-111">(Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").</span><span class="sxs-lookup"><span data-stu-id="b52de-111">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="b52de-112">Llame a [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para crear un objeto desencadenador.</span><span class="sxs-lookup"><span data-stu-id="b52de-112">Call [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) to create a trigger object.</span></span> <span data-ttu-id="b52de-113">(Tenga en cuenta que [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) se hereda de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)).</span><span class="sxs-lookup"><span data-stu-id="b52de-113">(Note that [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
4.  <span data-ttu-id="b52de-114">Defina una estructura de [**\_ desencadenador de tarea**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="b52de-114">Define a [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="b52de-115">Tenga en cuenta que los miembros wBeginDay, wBeginMonth y wBeginYear del **\_ desencadenador de tarea** deben establecerse en un día, un mes y un año válidos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b52de-115">Note that wBeginDay, wBeginMonth, and wBeginYear members of **TASK\_TRIGGER** must be set to a valid day, month, and year respectively.</span></span>
5.  <span data-ttu-id="b52de-116">Llame a [**ITaskTrigger:: SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) para establecer los criterios del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="b52de-116">Call [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) to set the trigger criteria.</span></span>
6.  <span data-ttu-id="b52de-117">Guarde la tarea con el nuevo desencadenador en el disco mediante [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="b52de-117">Save the task with the new trigger to disk using [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="b52de-118">(La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz com estándar compatible con la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) ).</span><span class="sxs-lookup"><span data-stu-id="b52de-118">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
7.  <span data-ttu-id="b52de-119">Llame a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="b52de-119">Call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release all resources.</span></span> <span data-ttu-id="b52de-120">(Tenga en cuenta que **Release** es un método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) heredado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).</span><span class="sxs-lookup"><span data-stu-id="b52de-120">(Note that **Release** is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="b52de-121">Para obtener un ejemplo de código de</span><span class="sxs-lookup"><span data-stu-id="b52de-121">For a code example of</span></span>                       | <span data-ttu-id="b52de-122">Vea</span><span class="sxs-lookup"><span data-stu-id="b52de-122">See</span></span>                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b52de-123">Crear un nuevo desencadenador para una tarea existente</span><span class="sxs-lookup"><span data-stu-id="b52de-123">Creating a new trigger for an existing task</span></span> | [<span data-ttu-id="b52de-124">Ejemplo de código de C/C++: creación de un desencadenador de tarea</span><span class="sxs-lookup"><span data-stu-id="b52de-124">C/C++ Code Example: Creating a Task Trigger</span></span>](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a><span data-ttu-id="b52de-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b52de-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b52de-126">Ejemplos de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="b52de-126">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 