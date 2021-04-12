---
title: Recuperación de ejemplos de propiedades de tarea
description: Para recuperar las propiedades de una tarea, llame a ITaskScheduler activate para obtener la recuperación de la interfaz del objeto de tarea y, a continuación, llame al método ITask adecuado para recuperar la propiedad de tarea que le interesa.
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- recuperación de las propiedades de la tarea Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2b42bc8044171834b6d99e97c41e3f5c7048ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359278"
---
# <a name="retrieving-task-property-examples"></a><span data-ttu-id="48272-104">Recuperación de ejemplos de propiedades de tarea</span><span class="sxs-lookup"><span data-stu-id="48272-104">Retrieving Task Property Examples</span></span>

<span data-ttu-id="48272-105">Para recuperar las propiedades de una tarea, llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la recuperación de la interfaz del objeto de tarea y, después, llame al método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) adecuado para recuperar la propiedad de tarea que le interesa.</span><span class="sxs-lookup"><span data-stu-id="48272-105">To retrieve the properties of a task, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get retrieve the interface of the task object, then call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to retrieve the task property that you are interested in.</span></span> <span data-ttu-id="48272-106">Los ejemplos de código que aparecen en la parte inferior de la página muestran cómo recuperar las distintas propiedades de tarea.</span><span class="sxs-lookup"><span data-stu-id="48272-106">The code examples listed at the bottom of the page show how to retrieve the different task properties.</span></span>

<span data-ttu-id="48272-107">Los ejemplos de código que aparecen en la parte inferior de la página muestran cómo recuperar las propiedades que son exclusivas de los objetos de tarea.</span><span class="sxs-lookup"><span data-stu-id="48272-107">The code examples listed at the bottom of the page show how to retrieve the properties that are unique to task objects.</span></span> <span data-ttu-id="48272-108">Para otras propiedades de [*elementos de trabajo*](w.md) que también se aplican a las tareas, vea [recuperar ejemplos de elementos de trabajo](retrieving-work-item-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="48272-108">For other [*work item*](w.md) properties that also apply to tasks, see [Retrieving Work Item Examples](retrieving-work-item-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="48272-109">En el ejemplo de código siguiente, todas las interfaces se liberan una vez que ya no se necesitan.</span><span class="sxs-lookup"><span data-stu-id="48272-109">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="48272-110">Tenga en cuenta que si va a recuperar una propiedad de cadena (como el nombre de la aplicación, los parámetros o el directorio de trabajo), debe llamar a [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria asignada para la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="48272-110">Note that if you are retrieving a string property (such as the application name, parameters, or working directory), you must call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>

<span data-ttu-id="48272-111">En el procedimiento siguiente se describe cómo recuperar una propiedad de tarea.</span><span class="sxs-lookup"><span data-stu-id="48272-111">The following procedure describes how to retrieve a task property.</span></span>

<span data-ttu-id="48272-112">**Para recuperar una propiedad de tarea**</span><span class="sxs-lookup"><span data-stu-id="48272-112">**To retrieve a task property**</span></span>

1.  <span data-ttu-id="48272-113">Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="48272-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="48272-114">(En estos ejemplos se supone que el servicio Programador de tareas se está ejecutando).</span><span class="sxs-lookup"><span data-stu-id="48272-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="48272-115">Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea.</span><span class="sxs-lookup"><span data-stu-id="48272-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="48272-116">(Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").</span><span class="sxs-lookup"><span data-stu-id="48272-116">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="48272-117">Llame al método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) adecuado para recuperar la propiedad que le interese.</span><span class="sxs-lookup"><span data-stu-id="48272-117">Call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to retrieve the property you are interested in.</span></span>
4.  <span data-ttu-id="48272-118">Procese la propiedad según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="48272-118">Process the property as needed.</span></span> <span data-ttu-id="48272-119">(Estos ejemplos imprimen la propiedad en la pantalla).</span><span class="sxs-lookup"><span data-stu-id="48272-119">(These examples print the property to the screen.)</span></span>
5.  <span data-ttu-id="48272-120">Si la propiedad devuelta es una cadena, llame a [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria asignada para la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="48272-120">If the returned property is a string, call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>



| <span data-ttu-id="48272-121">Para obtener un ejemplo de código de</span><span class="sxs-lookup"><span data-stu-id="48272-121">For a code example of</span></span>                                                                                                                           | <span data-ttu-id="48272-122">Vea</span><span class="sxs-lookup"><span data-stu-id="48272-122">See</span></span>                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48272-123">Recuperar el nombre de la aplicación asociada a una tarea determinada</span><span class="sxs-lookup"><span data-stu-id="48272-123">Retrieving the name of the application associated with a given task</span></span>                                                                             | [<span data-ttu-id="48272-124">Ejemplo de código de C/C++: recuperar el nombre de la aplicación de tarea</span><span class="sxs-lookup"><span data-stu-id="48272-124">C/C++ Code Example: Retrieving the Task Application Name</span></span>](c-c-code-example-retrieving-the-task-application-name.md)   |
| <span data-ttu-id="48272-125">Recuperar la cantidad máxima de tiempo que la tarea puede ejecutarse y mostrar ese número en la pantalla</span><span class="sxs-lookup"><span data-stu-id="48272-125">Retrieving the maximum amount of time the task can run and displaying that number on the screen</span></span>                                                 | [<span data-ttu-id="48272-126">Ejemplo de código de C/C++: recuperar la tarea MaxRunTime</span><span class="sxs-lookup"><span data-stu-id="48272-126">C/C++ Code Example: Retrieving the Task MaxRunTime</span></span>](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| <span data-ttu-id="48272-127">Recuperar la cadena de parámetro que se ejecuta cuando se ejecuta la tarea y mostrar esa cadena en la pantalla</span><span class="sxs-lookup"><span data-stu-id="48272-127">Retrieving the parameter string that is executed when the task is run and displaying that string on the screen</span></span>                                  | [<span data-ttu-id="48272-128">Ejemplo de código de C/C++: recuperar parámetros de tarea</span><span class="sxs-lookup"><span data-stu-id="48272-128">C/C++ Code Example: Retrieving Task Parameters</span></span>](c-c-code-example-retrieving-task-parameters.md)                       |
| <span data-ttu-id="48272-129">Recuperar el [*nivel de prioridad*](p.md) de la tarea</span><span class="sxs-lookup"><span data-stu-id="48272-129">Retrieving the [*priority level*](p.md) of the task</span></span>                                                                    | [<span data-ttu-id="48272-130">Ejemplo de código de C/C++: recuperar la prioridad de la tarea</span><span class="sxs-lookup"><span data-stu-id="48272-130">C/C++ Code Example: Retrieving Task Priority</span></span>](c-c-code-example-retrieving-task-priority.md)                           |
| <span data-ttu-id="48272-131">Recuperar el [*Directorio de trabajo*](w.md) de una tarea y mostrar la ruta de acceso al directorio de trabajo en la pantalla</span><span class="sxs-lookup"><span data-stu-id="48272-131">Retrieving the [*working directory*](w.md) of a task and displaying the path to the working directory on the screen</span></span> | [<span data-ttu-id="48272-132">Ejemplo de código de C/C++: recuperar el directorio de trabajo de la tarea</span><span class="sxs-lookup"><span data-stu-id="48272-132">C/C++ Code Example: Retrieving the Task Working Directory</span></span>](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a><span data-ttu-id="48272-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="48272-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48272-134">Ejemplos de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="48272-134">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 