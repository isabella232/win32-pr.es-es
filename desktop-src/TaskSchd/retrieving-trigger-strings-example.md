---
title: Ejemplo de recuperación de cadenas de desencadenador
description: Puede recuperar las cadenas de desencadenador de un desencadenador conocido mediante la interfaz IScheduledWorkItem o ITaskTrigger, en función del tipo de objeto con el que esté trabajando.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- recuperar cadenas de desencadenador Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44708fdbb4025f5d99409297dda65504a909aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685762"
---
# <a name="retrieving-trigger-strings-example"></a><span data-ttu-id="1d1aa-104">Ejemplo de recuperación de cadenas de desencadenador</span><span class="sxs-lookup"><span data-stu-id="1d1aa-104">Retrieving Trigger Strings Example</span></span>

<span data-ttu-id="1d1aa-105">Puede recuperar las cadenas de desencadenador de un desencadenador conocido mediante la interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) o [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) , en función del tipo de objeto con el que esté trabajando.</span><span class="sxs-lookup"><span data-stu-id="1d1aa-105">You can retrieve the trigger strings of a known trigger using the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) or [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface, depending on the type of object you are working with.</span></span>

<span data-ttu-id="1d1aa-106">Al trabajar con un [*objeto de tarea*](t.md), use los métodos de la interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) para recuperar las cadenas de desencadenador de un elemento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="1d1aa-106">When working with a [*task object*](t.md), use the methods of the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface to retrieve the trigger strings of a work item.</span></span>

<span data-ttu-id="1d1aa-107">Cuando trabaje con un objeto de [*desencadenador de tarea*](t.md), use los métodos de la interfaz [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) para recuperar la cadena de desencadenador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="1d1aa-107">When you are working with a [*task trigger object*](t.md), use the methods of the [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface to retrieve the trigger string of the trigger.</span></span>

<span data-ttu-id="1d1aa-108">En el ejemplo siguiente se muestra cómo usar [**IScheduledWorkItem:: GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) para mostrar las cadenas de todos los desencadenadores asociados a una tarea conocida.</span><span class="sxs-lookup"><span data-stu-id="1d1aa-108">The following example shows how to use [**IScheduledWorkItem::GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) to display the strings of all triggers associated with a known task.</span></span>

<span data-ttu-id="1d1aa-109">En el procedimiento siguiente se describe cómo recuperar las cadenas de desencadenador de una tarea.</span><span class="sxs-lookup"><span data-stu-id="1d1aa-109">The following procedure describes how to retrieve the trigger strings of a task.</span></span>

<span data-ttu-id="1d1aa-110">**Para recuperar las cadenas de desencadenador de una tarea**</span><span class="sxs-lookup"><span data-stu-id="1d1aa-110">**To retrieve the trigger strings of a task**</span></span>

1.  <span data-ttu-id="1d1aa-111">Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="1d1aa-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="1d1aa-112">(En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).</span><span class="sxs-lookup"><span data-stu-id="1d1aa-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="1d1aa-113">Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea.</span><span class="sxs-lookup"><span data-stu-id="1d1aa-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="1d1aa-114">(Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").</span><span class="sxs-lookup"><span data-stu-id="1d1aa-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="1d1aa-115">Llame a **ITask:: GetTriggerCount** para averiguar el número de desencadenadores asociados a una tarea.</span><span class="sxs-lookup"><span data-stu-id="1d1aa-115">Call **ITask::GetTriggerCount** to find out how many triggers are associated with a task.</span></span> <span data-ttu-id="1d1aa-116">(Tenga en cuenta que [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) es un método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) heredado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).</span><span class="sxs-lookup"><span data-stu-id="1d1aa-116">(Note that [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
4.  <span data-ttu-id="1d1aa-117">Mostrar las cadenas de desencadenador, llamando a **ITask:: GetTriggerString** para cada desencadenador asociado a la tarea.</span><span class="sxs-lookup"><span data-stu-id="1d1aa-117">Display the trigger strings, calling **ITask::GetTriggerString** for each trigger associated with the task.</span></span> <span data-ttu-id="1d1aa-118">(Tenga en cuenta que [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) es un método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) heredado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).</span><span class="sxs-lookup"><span data-stu-id="1d1aa-118">(Note that [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
5.  <span data-ttu-id="1d1aa-119">Libera todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="1d1aa-119">Release all resources.</span></span> <span data-ttu-id="1d1aa-120">Llame a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar las cadenas del desencadenador y **ITask:: Release** para liberar la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="1d1aa-120">Call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the trigger strings and **ITask::Release** to release the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="1d1aa-121">(Tenga en cuenta que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) es un método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) heredado por **ITask**).</span><span class="sxs-lookup"><span data-stu-id="1d1aa-121">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by **ITask**.)</span></span>



| <span data-ttu-id="1d1aa-122">Para obtener un ejemplo de código de</span><span class="sxs-lookup"><span data-stu-id="1d1aa-122">For a code example of</span></span>                                                         | <span data-ttu-id="1d1aa-123">Vea</span><span class="sxs-lookup"><span data-stu-id="1d1aa-123">See</span></span>                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d1aa-124">Recuperar una cadena de desencadenador para todos los desencadenadores asociados a una tarea conocida</span><span class="sxs-lookup"><span data-stu-id="1d1aa-124">Retrieving a trigger string for all the triggers associated with a known task</span></span> | [<span data-ttu-id="1d1aa-125">Ejemplo de código: recuperar cadenas de desencadenador</span><span class="sxs-lookup"><span data-stu-id="1d1aa-125">Code Example: Retrieving Trigger Strings</span></span>](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a><span data-ttu-id="1d1aa-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d1aa-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d1aa-127">Ejemplos de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="1d1aa-127">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 