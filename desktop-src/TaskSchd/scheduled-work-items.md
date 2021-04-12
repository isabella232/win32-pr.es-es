---
title: Elementos de trabajo programados
description: En el Programador de tareas se usan dos términos para describir lo que puede programar elementos de trabajo y tareas.
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- Programador de tareas de elementos de trabajo
- Programador de tareas de elementos de trabajo, en comparación con las tareas
- Programador de tareas de tareas
- tareas Programador de tareas, comparación con los elementos de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586747e4049529dcfe747959aae994360a7b1485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356935"
---
# <a name="scheduled-work-items"></a><span data-ttu-id="12f29-107">Elementos de trabajo programados</span><span class="sxs-lookup"><span data-stu-id="12f29-107">Scheduled Work Items</span></span>

<span data-ttu-id="12f29-108">En el Programador de tareas se usan dos términos para describir lo que puede programar: elementos de trabajo y tareas.</span><span class="sxs-lookup"><span data-stu-id="12f29-108">The Task Scheduler uses two terms to describe what it can schedule: work items and tasks.</span></span> <span data-ttu-id="12f29-109">De estos dos términos, [*elemento de trabajo*](w.md) es un término más general que describe cualquier tipo de elemento que se puede programar.</span><span class="sxs-lookup"><span data-stu-id="12f29-109">Of these two terms, [*work item*](w.md) is a more general term that describes any type of item that can be scheduled.</span></span> <span data-ttu-id="12f29-110">Un *elemento de trabajo* puede ser cualquier elemento que el servicio Programador de tareas se ejecute a la vez que se especifica en los desencadenadores del elemento.</span><span class="sxs-lookup"><span data-stu-id="12f29-110">A *work item* can be any item that the Task Scheduler service runs at a time that is specified by the item's trigger(s).</span></span>

<span data-ttu-id="12f29-111">Por el contrario, una [*tarea*](t.md) es un tipo específico de elemento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="12f29-111">In contrast, a [*task*](t.md) is a specific type of work item.</span></span> <span data-ttu-id="12f29-112">Actualmente, el único tipo de elemento de trabajo programado que se admite es una tarea.</span><span class="sxs-lookup"><span data-stu-id="12f29-112">Currently, the only type of scheduled work item that is supported is a task.</span></span>

<span data-ttu-id="12f29-113">La interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) contiene métodos que son compatibles con todos los tipos de elementos de trabajo programados.</span><span class="sxs-lookup"><span data-stu-id="12f29-113">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface contains methods that are supported by all types of scheduled work items.</span></span> <span data-ttu-id="12f29-114">Por ejemplo, la información de la cuenta, los tiempos de ejecución y los comentarios definidos por la aplicación son propiedades que se pueden aplicar a todos los tipos de elementos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="12f29-114">For example, account information, run times, and application-defined comments are properties that may apply to all types of work items.</span></span> <span data-ttu-id="12f29-115">Estas propiedades se pueden establecer y recuperar a través de la interfaz **IScheduledWorkItem** .</span><span class="sxs-lookup"><span data-stu-id="12f29-115">These properties can be set and retrieved through the **IScheduledWorkItem** interface.</span></span>

<span data-ttu-id="12f29-116">La interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) contiene métodos que solo son compatibles con las tareas.</span><span class="sxs-lookup"><span data-stu-id="12f29-116">The [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface contains methods that are supported only by tasks.</span></span>

<span data-ttu-id="12f29-117">Los métodos de la interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) los hereda actualmente la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) y, en el futuro, las heredarán otras interfaces de elementos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="12f29-117">The methods of the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface are currently inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface and in the future will be inherited by other work item interfaces.</span></span>

| <span data-ttu-id="12f29-118">Para obtener ejemplos de</span><span class="sxs-lookup"><span data-stu-id="12f29-118">For examples of</span></span>                                              | <span data-ttu-id="12f29-119">Vea</span><span class="sxs-lookup"><span data-stu-id="12f29-119">See</span></span>                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="12f29-120">Crear una nueva tarea.</span><span class="sxs-lookup"><span data-stu-id="12f29-120">Creating a new task.</span></span>                                         | [<span data-ttu-id="12f29-121">Crear una tarea mediante el ejemplo NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="12f29-121">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) |
| <span data-ttu-id="12f29-122">Ejecutar una tarea existente.</span><span class="sxs-lookup"><span data-stu-id="12f29-122">Running an existing task.</span></span>                                    | [<span data-ttu-id="12f29-123">Ejemplo de inicio de una tarea</span><span class="sxs-lookup"><span data-stu-id="12f29-123">Starting a Task Example</span></span>](starting-a-task-example.md)                                     |
| <span data-ttu-id="12f29-124">Recuperando propiedades que se aplican a todos los tipos de elementos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="12f29-124">Retrieving properties that apply to all types of work items.</span></span> | [<span data-ttu-id="12f29-125">Recuperar ejemplos de propiedades de elementos de trabajo</span><span class="sxs-lookup"><span data-stu-id="12f29-125">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       |
| <span data-ttu-id="12f29-126">Establecer las propiedades que se aplican a todos los tipos de elementos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="12f29-126">Setting properties that apply to all types of work items.</span></span>    | [<span data-ttu-id="12f29-127">Configuración de ejemplos de propiedades de elementos de trabajo</span><span class="sxs-lookup"><span data-stu-id="12f29-127">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             |



 

 

 




