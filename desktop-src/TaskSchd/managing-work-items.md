---
title: Manipular elementos de trabajo
description: La interfaz IScheduledWorkItem proporciona métodos para recuperar y establecer las propiedades de los elementos de trabajo. crear, recuperar y eliminar desencadenadores de elementos de trabajo (el establecimiento del desencadenador debe realizarse con el método ITaskTrigger SetTrigger); y para ejecutar, finalizar y eliminar el elemento de trabajo. Nota para las propiedades de un tipo específico de elemento de trabajo, consulte la interfaz para ese tipo de objeto. Por ejemplo, no se puede establecer el nivel de prioridad de un elemento de trabajo; sin embargo, puede usar los métodos de la interfaz ITask para recuperar y establecer la prioridad de una tarea.
ms.assetid: 8aedf96d-e43d-4aac-ad8c-860379209f95
keywords:
- Programador de tareas de elementos de trabajo, administrar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33680d04da9d34f54085d182ed61edda9e8b232f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792561"
---
# <a name="manipulating-work-items"></a><span data-ttu-id="d65d3-105">Manipular elementos de trabajo</span><span class="sxs-lookup"><span data-stu-id="d65d3-105">Manipulating Work Items</span></span>

<span data-ttu-id="d65d3-106">La interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) proporciona métodos para recuperar y establecer las propiedades de los elementos de trabajo. crear, recuperar y eliminar desencadenadores de elementos de trabajo (el establecimiento del desencadenador debe realizarse con el método [**ITaskTrigger:: SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) ); y para ejecutar, finalizar y eliminar el elemento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d65d3-106">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface provides methods for retrieving and setting work item properties; creating, retrieving, and deleting triggers for work items (setting the trigger must be done with the [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) method); and for running, terminating, and deleting the work item.</span></span>

> [!Note]  
> <span data-ttu-id="d65d3-107">En el caso de las propiedades de un tipo específico de elemento de trabajo, consulte la interfaz para ese tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="d65d3-107">For the properties of a specific type of work item, refer to the interface for that type of object.</span></span> <span data-ttu-id="d65d3-108">Por ejemplo, no se puede establecer el nivel de prioridad de un elemento de trabajo; sin embargo, puede usar los métodos de la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) para recuperar y establecer la prioridad de una tarea.</span><span class="sxs-lookup"><span data-stu-id="d65d3-108">For example, you cannot set the priority level of a work item; however, you can use the methods of the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface to retrieve and set the priority of a task.</span></span>

 

<span data-ttu-id="d65d3-109">Siempre que modifique un elemento de trabajo, debe llamar al objeto [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para guardar el elemento de trabajo modificado en el disco.</span><span class="sxs-lookup"><span data-stu-id="d65d3-109">Whenever you modify a work item, you must call the [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) object to save the modified work item to disk.</span></span> <span data-ttu-id="d65d3-110">La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz com estándar que es compatible con la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="d65d3-110">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface that is supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>

| <span data-ttu-id="d65d3-111">Para obtener ejemplos de</span><span class="sxs-lookup"><span data-stu-id="d65d3-111">For examples of</span></span>                                                            | <span data-ttu-id="d65d3-112">Vea</span><span class="sxs-lookup"><span data-stu-id="d65d3-112">See</span></span>                                                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d65d3-113">Recuperar propiedades que se aplican a todos los tipos de elementos de trabajo</span><span class="sxs-lookup"><span data-stu-id="d65d3-113">Retrieving properties that apply to all types of work items</span></span>                | [<span data-ttu-id="d65d3-114">Recuperar ejemplos de propiedades de elementos de trabajo</span><span class="sxs-lookup"><span data-stu-id="d65d3-114">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md) |
| <span data-ttu-id="d65d3-115">Establecer propiedades que se aplican a todos los tipos de elementos de trabajo</span><span class="sxs-lookup"><span data-stu-id="d65d3-115">Setting properties that apply to all types of work items</span></span>                   | [<span data-ttu-id="d65d3-116">Configuración de ejemplos de propiedades de elementos de trabajo</span><span class="sxs-lookup"><span data-stu-id="d65d3-116">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)       |
| <span data-ttu-id="d65d3-117">Ejecución de una tarea conocida</span><span class="sxs-lookup"><span data-stu-id="d65d3-117">Running a known task</span></span>                                                       | [<span data-ttu-id="d65d3-118">Ejemplo de inicio de una tarea</span><span class="sxs-lookup"><span data-stu-id="d65d3-118">Starting a Task Example</span></span>](starting-a-task-example.md)                               |
| <span data-ttu-id="d65d3-119">Finalizar una tarea en ejecución</span><span class="sxs-lookup"><span data-stu-id="d65d3-119">Terminating a running task</span></span>                                                 | [<span data-ttu-id="d65d3-120">Ejemplo de finalización de una tarea</span><span class="sxs-lookup"><span data-stu-id="d65d3-120">Terminating a Task Example</span></span>](terminating-a-task-example.md)                         |
| <span data-ttu-id="d65d3-121">Crear un nuevo desencadenador para una tarea conocida</span><span class="sxs-lookup"><span data-stu-id="d65d3-121">Creating a new trigger for a known task</span></span>                                    | [<span data-ttu-id="d65d3-122">Crear un nuevo desencadenador</span><span class="sxs-lookup"><span data-stu-id="d65d3-122">Creating a New Trigger</span></span>](creating-a-new-trigger.md)                                 |
| <span data-ttu-id="d65d3-123">Crear un desencadenador de inactividad basado en eventos para una tarea conocida</span><span class="sxs-lookup"><span data-stu-id="d65d3-123">Creating an event-based idle trigger for a known task</span></span>                      | [<span data-ttu-id="d65d3-124">Ejemplo de creación de un desencadenador inactivo</span><span class="sxs-lookup"><span data-stu-id="d65d3-124">Creating an Idle Trigger Example</span></span>](creating-an-idle-trigger-example.md)             |
| <span data-ttu-id="d65d3-125">Recuperar la cadena de desencadenador de todos los desencadenadores asociados a una tarea conocida</span><span class="sxs-lookup"><span data-stu-id="d65d3-125">Retrieving the trigger string of all triggers associated with a known task</span></span> | [<span data-ttu-id="d65d3-126">Ejemplo de recuperación de cadenas de desencadenador</span><span class="sxs-lookup"><span data-stu-id="d65d3-126">Retrieving Trigger Strings Example</span></span>](retrieving-trigger-strings-example.md)         |



 

 

 