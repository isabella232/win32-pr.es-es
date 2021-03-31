---
title: Configuración de ejemplos de propiedades de elementos de trabajo
description: Para establecer las propiedades de un elemento de trabajo, llame a ITaskScheduler activate para recuperar la interfaz del objeto de elemento de trabajo y, a continuación, llame al método adecuado para establecer la propiedad de tarea que le interese. Actualmente, los únicos elementos de trabajo válidos son tareas.
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- establecer las propiedades de los elementos de trabajo Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e026ea3d2b3f6677a3d229e9289ab9b201e02b94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995470"
---
# <a name="setting-work-item-property-examples"></a><span data-ttu-id="ffdc9-105">Configuración de ejemplos de propiedades de elementos de trabajo</span><span class="sxs-lookup"><span data-stu-id="ffdc9-105">Setting Work Item Property Examples</span></span>

<span data-ttu-id="ffdc9-106">Para establecer las propiedades de un elemento de trabajo, llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para recuperar la interfaz del objeto de elemento de trabajo y, a continuación, llame al método adecuado para establecer la propiedad de tarea que le interese.</span><span class="sxs-lookup"><span data-stu-id="ffdc9-106">To set the properties of a work item, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the work item object, then call the appropriate method to set the task property you are interested in.</span></span> <span data-ttu-id="ffdc9-107">Actualmente, los únicos elementos de trabajo válidos son tareas.</span><span class="sxs-lookup"><span data-stu-id="ffdc9-107">Currently, the only valid work items are tasks.</span></span>

<span data-ttu-id="ffdc9-108">Los ejemplos de código que aparecen en la parte inferior de la página muestran cómo establecer las propiedades que se aplican a todos los elementos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ffdc9-108">The code examples listed at the bottom of the page show how to set the properties that apply to all work items.</span></span> <span data-ttu-id="ffdc9-109">Para otras propiedades que son exclusivas de las tareas, consulte Configuración de los [ejemplos de propiedades de tarea](setting-task-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="ffdc9-109">For other properties that are unique to tasks, see [Setting Task Property Examples](setting-task-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="ffdc9-110">En el ejemplo de código siguiente, todas las interfaces se liberan una vez que ya no se necesitan.</span><span class="sxs-lookup"><span data-stu-id="ffdc9-110">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="ffdc9-111">En los ejemplos siguientes, el objeto modificado siempre se guarda en el disco mediante una llamada a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="ffdc9-111">In the following examples, the modified object is always saved to disk by a call to [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="ffdc9-112">(La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz com estándar heredada por el objeto de tarea).</span><span class="sxs-lookup"><span data-stu-id="ffdc9-112">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface inherited by the task object.)</span></span>

<span data-ttu-id="ffdc9-113">En el procedimiento siguiente se describe cómo establecer una propiedad de tarea.</span><span class="sxs-lookup"><span data-stu-id="ffdc9-113">The following procedure describes how to set a task property.</span></span>

<span data-ttu-id="ffdc9-114">**Para establecer una propiedad de tarea**</span><span class="sxs-lookup"><span data-stu-id="ffdc9-114">**To set a task property**</span></span>

1.  <span data-ttu-id="ffdc9-115">Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="ffdc9-115">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="ffdc9-116">(En estos ejemplos se supone que el servicio Programador de tareas se está ejecutando).</span><span class="sxs-lookup"><span data-stu-id="ffdc9-116">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="ffdc9-117">Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea.</span><span class="sxs-lookup"><span data-stu-id="ffdc9-117">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="ffdc9-118">(Tenga en cuenta que las tareas son actualmente el único tipo válido de elemento de trabajo).</span><span class="sxs-lookup"><span data-stu-id="ffdc9-118">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="ffdc9-119">Llame al método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) adecuado para establecer la propiedad que le interese.</span><span class="sxs-lookup"><span data-stu-id="ffdc9-119">Call the appropriate [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method to set the property you are interested in.</span></span> <span data-ttu-id="ffdc9-120">Tenga en cuenta que la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) hereda los métodos **IScheduledWorkItem** .</span><span class="sxs-lookup"><span data-stu-id="ffdc9-120">Note that **IScheduledWorkItem** methods are inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>
4.  <span data-ttu-id="ffdc9-121">Llame a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para almacenar el objeto de tarea modificado en el disco.</span><span class="sxs-lookup"><span data-stu-id="ffdc9-121">Call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to store the modified task object to disk.</span></span>



| <span data-ttu-id="ffdc9-122">Para obtener un ejemplo de código de</span><span class="sxs-lookup"><span data-stu-id="ffdc9-122">For a code example of</span></span>                            | <span data-ttu-id="ffdc9-123">Vea</span><span class="sxs-lookup"><span data-stu-id="ffdc9-123">See</span></span>                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffdc9-124">Establecer la información de la cuenta para una tarea conocida</span><span class="sxs-lookup"><span data-stu-id="ffdc9-124">Setting the account information for a known task</span></span> | [<span data-ttu-id="ffdc9-125">Ejemplo de código de C/C++: establecer la información de la cuenta de tarea</span><span class="sxs-lookup"><span data-stu-id="ffdc9-125">C/C++ Code Example: Setting Task Account Information</span></span>](c-c-code-example-setting-task-account-information.md) |
| <span data-ttu-id="ffdc9-126">Establecer el comentario de una tarea conocida</span><span class="sxs-lookup"><span data-stu-id="ffdc9-126">Setting the comment of a known task</span></span>              | [<span data-ttu-id="ffdc9-127">Ejemplo de código de C/C++: establecer comentario de tarea</span><span class="sxs-lookup"><span data-stu-id="ffdc9-127">C/C++ Code Example: Setting Task Comment</span></span>](c-c-code-example-setting-task-comment.md)                         |



 

## <a name="related-topics"></a><span data-ttu-id="ffdc9-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ffdc9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffdc9-129">Ejemplos de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="ffdc9-129">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 