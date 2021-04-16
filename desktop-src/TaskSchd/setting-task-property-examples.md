---
title: Configuración de ejemplos de propiedades de tarea
description: Para establecer las propiedades de una tarea, llame a ITaskScheduler activate para recuperar la interfaz del objeto de tarea y, después, llame al método ITask adecuado para establecer la propiedad de tarea que le interese.
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- establecer las propiedades de la tarea Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb05031961e38314cbc7cd12c20c1d863f54af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685764"
---
# <a name="setting-task-property-examples"></a><span data-ttu-id="fd04d-104">Configuración de ejemplos de propiedades de tarea</span><span class="sxs-lookup"><span data-stu-id="fd04d-104">Setting Task Property Examples</span></span>

<span data-ttu-id="fd04d-105">Para establecer las propiedades de una tarea, llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para recuperar la interfaz del objeto de tarea y, después, llame al método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) adecuado para establecer la propiedad de tarea que le interese.</span><span class="sxs-lookup"><span data-stu-id="fd04d-105">To set the properties of a task, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the task object, then call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to set the task property you are interested in.</span></span>

<span data-ttu-id="fd04d-106">Los ejemplos de código que aparecen en la parte inferior de la página muestran cómo establecer las propiedades que son exclusivas de los objetos de tarea.</span><span class="sxs-lookup"><span data-stu-id="fd04d-106">The code examples listed at the bottom of the page show how to set the properties that are unique to task objects.</span></span> <span data-ttu-id="fd04d-107">Para otras propiedades de [*elementos de trabajo*](w.md) que también se aplican a las tareas, vea [establecer ejemplos de propiedades de elementos de trabajo](setting-work-item-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="fd04d-107">For other [*work item*](w.md) properties that also apply to tasks, see [Setting Work Item Property Examples](setting-work-item-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="fd04d-108">En el ejemplo de código siguiente, todas las interfaces se liberan una vez que ya no se necesitan.</span><span class="sxs-lookup"><span data-stu-id="fd04d-108">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="fd04d-109">En los ejemplos siguientes, el objeto de tarea modificado siempre se guarda en el disco mediante una llamada a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="fd04d-109">In the following examples, the modified task object is always saved to disk by a call to [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="fd04d-110">(La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) es una interfaz com estándar heredada por el objeto de tarea).</span><span class="sxs-lookup"><span data-stu-id="fd04d-110">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface inherited by the task object.)</span></span>

<span data-ttu-id="fd04d-111">En el procedimiento siguiente se describe cómo establecer una propiedad de tarea.</span><span class="sxs-lookup"><span data-stu-id="fd04d-111">The following procedure describes how to set a task property.</span></span>

<span data-ttu-id="fd04d-112">**Para establecer una propiedad de tarea**</span><span class="sxs-lookup"><span data-stu-id="fd04d-112">**To set a task property**</span></span>

1.  <span data-ttu-id="fd04d-113">Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="fd04d-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="fd04d-114">(En estos ejemplos se supone que el servicio Programador de tareas se está ejecutando).</span><span class="sxs-lookup"><span data-stu-id="fd04d-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="fd04d-115">Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea.</span><span class="sxs-lookup"><span data-stu-id="fd04d-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="fd04d-116">(Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").</span><span class="sxs-lookup"><span data-stu-id="fd04d-116">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="fd04d-117">Llame al método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) adecuado para establecer la propiedad que le interese.</span><span class="sxs-lookup"><span data-stu-id="fd04d-117">Call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to set the property you are interested in.</span></span>
4.  <span data-ttu-id="fd04d-118">Llame a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para almacenar el objeto de tarea modificado en el disco.</span><span class="sxs-lookup"><span data-stu-id="fd04d-118">Call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to store the modified task object to disk.</span></span>



| <span data-ttu-id="fd04d-119">Para obtener un ejemplo de código de</span><span class="sxs-lookup"><span data-stu-id="fd04d-119">For a code example of</span></span>                                                                                                                                | <span data-ttu-id="fd04d-120">Vea</span><span class="sxs-lookup"><span data-stu-id="fd04d-120">See</span></span>                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd04d-121">Establecer el nombre de la aplicación asociada a una tarea conocida</span><span class="sxs-lookup"><span data-stu-id="fd04d-121">Setting the name of the application associated with a known task</span></span>                                                                                     | [<span data-ttu-id="fd04d-122">Ejemplo de código de C/C++: establecer el nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="fd04d-122">C/C++ Code Example: Setting Application Name</span></span>](c-c-code-example-setting-application-name.md)   |
| <span data-ttu-id="fd04d-123">Establecer el tiempo de ejecución máximo de una tarea conocida</span><span class="sxs-lookup"><span data-stu-id="fd04d-123">Setting the maximum run time of a known task</span></span>                                                                                                         | [<span data-ttu-id="fd04d-124">Ejemplo de código de C/C++: establecer MaxRunTime</span><span class="sxs-lookup"><span data-stu-id="fd04d-124">C/C++ Code Example: Setting MaxRunTime</span></span>](c-c-code-example-setting-maxruntime.md)               |
| <span data-ttu-id="fd04d-125">Borrar todos los parámetros de línea de comandos asociados a una tarea conocida</span><span class="sxs-lookup"><span data-stu-id="fd04d-125">Clearing all command-line parameters associated with a known task</span></span>                                                                                    | [<span data-ttu-id="fd04d-126">Ejemplo de código de C/C++: establecer parámetros de tarea</span><span class="sxs-lookup"><span data-stu-id="fd04d-126">C/C++ Code Example: Setting Task Parameters</span></span>](c-c-code-example-setting-task-parameters.md)     |
| <span data-ttu-id="fd04d-127">En este ejemplo se establece la prioridad de una tarea de prueba y, a continuación, se guarda la tarea.</span><span class="sxs-lookup"><span data-stu-id="fd04d-127">This example sets the priority of a test task and then saves the task.</span></span> <span data-ttu-id="fd04d-128">En este ejemplo se da por supuesto que la tarea de prueba ya existe en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="fd04d-128">This example assumes that the test task already exists on the local computer.</span></span> | [<span data-ttu-id="fd04d-129">Ejemplo de código de C/C++: establecer la prioridad de la tarea</span><span class="sxs-lookup"><span data-stu-id="fd04d-129">C/C++ Code Example: Setting Task Priority</span></span>](c-c-code-example-setting-task-priority.md)         |
| <span data-ttu-id="fd04d-130">Establecer el [*Directorio de trabajo*](w.md) de una tarea conocida</span><span class="sxs-lookup"><span data-stu-id="fd04d-130">Setting the [*working directory*](w.md) of a known task</span></span>                                                                  | [<span data-ttu-id="fd04d-131">Ejemplo de código de C/C++: establecer el directorio de trabajo</span><span class="sxs-lookup"><span data-stu-id="fd04d-131">C/C++ Code Example: Setting Working Directory</span></span>](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a><span data-ttu-id="fd04d-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd04d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd04d-133">Ejemplos de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="fd04d-133">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 