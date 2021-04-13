---
title: Interfaces de desencadenador
description: Las API que se usan para administrar los desencadenadores varían en función de la versión de la Programador de tareas. Sin embargo, en ambos casos estas API le permiten crear nuevos desencadenadores, recuperar y actualizar los desencadenadores existentes, y eliminar los desencadenadores que ya no son necesarios.
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- desencadenadores Programador de tareas, interfaces
- desencadenadores Programador de tareas, interfaces, descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5357bb745b43c51707d9571c7582a44c9225a7fe
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104359534"
---
# <a name="trigger-interfaces"></a><span data-ttu-id="303b6-106">Interfaces de desencadenador</span><span class="sxs-lookup"><span data-stu-id="303b6-106">Trigger Interfaces</span></span>

<span data-ttu-id="303b6-107">Las API que se usan para administrar los desencadenadores varían en función de la versión de la Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="303b6-107">The APIs that are used to manage triggers vary depending on the version of the Task Scheduler.</span></span> <span data-ttu-id="303b6-108">Sin embargo, en ambos casos estas API le permiten crear nuevos desencadenadores, recuperar y actualizar los desencadenadores existentes, y eliminar los desencadenadores que ya no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="303b6-108">However, in both cases these APIs enable you to create new triggers, retrieve and update existing triggers, and delete triggers that are no longer required.</span></span>


<span data-ttu-id="303b6-109">Las aplicaciones desarrolladas con Programador de tareas 2,0 pueden utilizar objetos e interfaces para crear, recuperar, modificar y eliminar los desencadenadores de una tarea.</span><span class="sxs-lookup"><span data-stu-id="303b6-109">Applications that are developed using Task Scheduler 2.0 can use objects and interfaces to create, retrieve, modify, and delete the triggers for a task.</span></span>

<span data-ttu-id="303b6-110">En la ilustración siguiente, una tarea especifica una colección de desencadenadores mediante su propiedad Triggers.</span><span class="sxs-lookup"><span data-stu-id="303b6-110">In the following illustration, a task specifies a collection of triggers using its Triggers property.</span></span> <span data-ttu-id="303b6-111">Esta colección contiene una o varias API de desencadenador individual con cada API que especifica un tipo de desencadenador específico.</span><span class="sxs-lookup"><span data-stu-id="303b6-111">This collection contains one or more individual trigger APIs with each API specifying a specific trigger type.</span></span> <span data-ttu-id="303b6-112">Por ejemplo, en la ilustración siguiente, la colección de desencadenadores contiene un desencadenador de arranque, un desencadenador de inicio de sesión y un desencadenador diario.</span><span class="sxs-lookup"><span data-stu-id="303b6-112">For example, in the illustration below the trigger collection contains a boot trigger, logon trigger, and a daily trigger.</span></span>

![interfaces de desencadenador del programador de tareas 2,0](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a><span data-ttu-id="303b6-114">API de objetos para el desarrollo de scripting</span><span class="sxs-lookup"><span data-stu-id="303b6-114">Object APIs for Scripting Development</span></span>

<span data-ttu-id="303b6-115">Para obtener más información sobre los métodos y las propiedades de los objetos que se usan para especificar los desencadenadores, vea:</span><span class="sxs-lookup"><span data-stu-id="303b6-115">For more information about the methods and properties of the objects that are used to specify triggers, see:</span></span>

-   [<span data-ttu-id="303b6-116">**TaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="303b6-116">**TaskDefinition**</span></span>](taskdefinition.md)
-   [<span data-ttu-id="303b6-117">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="303b6-117">**TriggerCollection**</span></span>](triggercollection.md)
-   [<span data-ttu-id="303b6-118">**Activado**</span><span class="sxs-lookup"><span data-stu-id="303b6-118">**Trigger**</span></span>](trigger.md)
-   [<span data-ttu-id="303b6-119">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-119">**BootTrigger**</span></span>](boottrigger.md)
-   [<span data-ttu-id="303b6-120">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-120">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="303b6-121">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-121">**EventTrigger**</span></span>](eventtrigger.md)
-   [<span data-ttu-id="303b6-122">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-122">**IdleTrigger**</span></span>](idletrigger.md)
-   [<span data-ttu-id="303b6-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-123">**LogonTrigger**</span></span>](logontrigger.md)
-   [<span data-ttu-id="303b6-124">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-124">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
-   [<span data-ttu-id="303b6-125">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-125">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="303b6-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-126">**RegistrationTrigger**</span></span>](registrationtrigger.md)
-   [<span data-ttu-id="303b6-127">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-127">**TimeTrigger**</span></span>](timetrigger.md)
-   [<span data-ttu-id="303b6-128">**WeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-128">**WeeklyTrigger**</span></span>](weeklytrigger.md)

### <a name="interfaces-apis-for-c-development"></a><span data-ttu-id="303b6-129">Interfaces API para el desarrollo en C++</span><span class="sxs-lookup"><span data-stu-id="303b6-129">Interfaces APIs for C++ Development</span></span>

<span data-ttu-id="303b6-130">Para obtener más información sobre los métodos y las propiedades de las interfaces que se usan para especificar los desencadenadores, vea:</span><span class="sxs-lookup"><span data-stu-id="303b6-130">For more information about the methods and properties of the interfaces that are used to specify triggers, see:</span></span>

-   [<span data-ttu-id="303b6-131">**ITaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="303b6-131">**ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
-   [<span data-ttu-id="303b6-132">**ITriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="303b6-132">**ITriggerCollection**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)
-   [<span data-ttu-id="303b6-133">**ITrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-133">**ITrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itrigger)
-   [<span data-ttu-id="303b6-134">**IBootTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-134">**IBootTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)
-   [<span data-ttu-id="303b6-135">**IDailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-135">**IDailyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [<span data-ttu-id="303b6-136">**IEventTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-136">**IEventTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)
-   [<span data-ttu-id="303b6-137">**IIdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-137">**IIdleTrigger**</span></span>](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)
-   [<span data-ttu-id="303b6-138">**ILogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-138">**ILogonTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)
-   [<span data-ttu-id="303b6-139">**IMonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-139">**IMonthlyDOWTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)
-   [<span data-ttu-id="303b6-140">**IMonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-140">**IMonthlyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [<span data-ttu-id="303b6-141">**IRegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-141">**IRegistrationTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)
-   [<span data-ttu-id="303b6-142">**ITimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-142">**ITimeTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)
-   [<span data-ttu-id="303b6-143">**IWeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="303b6-143">**IWeeklyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="task-scheduler-10-trigger-interfaces"></a><span data-ttu-id="303b6-144">Interfaces de desencadenador de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="303b6-144">Task Scheduler 1.0 Trigger Interfaces</span></span>

<span data-ttu-id="303b6-145">Las aplicaciones existentes desarrolladas con Programador de tareas 1,0 pueden usar los métodos que están disponibles en las interfaces de Programador de tareas 1,0 para crear, recuperar, modificar y eliminar los desencadenadores de un [*elemento de trabajo*](w.md).</span><span class="sxs-lookup"><span data-stu-id="303b6-145">Existing applications that are developed using Task Scheduler 1.0 can use the methods that are available from the Task Scheduler 1.0 interfaces to create, retrieve, modify, and delete the triggers for a [*work item*](w.md).</span></span> <span data-ttu-id="303b6-146">Sin embargo, tenga en cuenta que todas las interfaces Programador de tareas 1,0, enumeraciones y estructuras están obsoletas y no deben usarse para el desarrollo de nuevas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="303b6-146">However, note that all Task Scheduler 1.0 interfaces, enumerations, and structures are obsolete and should not be used for the development of new applications.</span></span>

<span data-ttu-id="303b6-147">En la ilustración siguiente se muestran las dos interfaces que se usan para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="303b6-147">The two interfaces that are used to do this are shown in the following illustration.</span></span> <span data-ttu-id="303b6-148">La interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) se usa para administrar todos los desencadenadores asociados a un elemento de trabajo (tal administración incluye la creación de un nuevo desencadenador para el elemento de trabajo).</span><span class="sxs-lookup"><span data-stu-id="303b6-148">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface is used to manage all the triggers that are associated with a work item (such management includes creating a new trigger for the work item).</span></span> <span data-ttu-id="303b6-149">La interfaz [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) se usa para administrar un desencadenador específico.</span><span class="sxs-lookup"><span data-stu-id="303b6-149">The [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface is used to manage a specific trigger.</span></span>

![interfaces de desencadenador del programador de tareas 1,0](images/tsktri2.png)

<span data-ttu-id="303b6-151">La interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) proporciona métodos para crear un nuevo desencadenador para un elemento de trabajo, recuperar el número de desencadenadores asociados a un elemento de trabajo, recuperar las [*estructuras de desencadenador*](t.md) asociadas al elemento de trabajo, recuperar cadenas de [*desencadenador*](t.md) asociadas al elemento de trabajo y eliminar desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="303b6-151">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface provides methods for creating a new trigger for a work item, retrieving the number of triggers that are associated with a work item, retrieving the [*trigger structures*](t.md) that are associated with the work item, retrieving [*trigger strings*](t.md) that are associated with the work item, and for deleting triggers.</span></span>

<span data-ttu-id="303b6-152">Una vez que el objeto de desencadenador está disponible, puede usar la interfaz [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) para recuperar la estructura del desencadenador y la cadena del desencadenador y para establecer los criterios que se utilizan para activar el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="303b6-152">Once the trigger object is available, you can use the [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface to retrieve the trigger structure and the string of the trigger and to set the criteria that is used to fire the trigger.</span></span> <span data-ttu-id="303b6-153">Esta interfaz solo se usa cuando se trabaja con un [*objeto de desencadenador de tarea*](t.md).</span><span class="sxs-lookup"><span data-stu-id="303b6-153">This interface is used only when you are working with a [*task trigger object*](t.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="303b6-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="303b6-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="303b6-155">Desencadenadores de tareas</span><span class="sxs-lookup"><span data-stu-id="303b6-155">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="303b6-156">Tipos de desencadenador</span><span class="sxs-lookup"><span data-stu-id="303b6-156">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="303b6-157">Estructuras de desencadenador</span><span class="sxs-lookup"><span data-stu-id="303b6-157">Trigger Structures</span></span>](trigger-structures.md)
</dt> </dl>

 

 