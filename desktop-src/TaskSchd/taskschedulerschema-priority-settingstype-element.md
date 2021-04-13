---
title: Elemento Priority (settingsType)
description: Especifica el nivel de prioridad de la tarea.
ms.assetid: 4885fffa-b7d9-4f5e-b6e8-6f18b01c2427
keywords:
- Elemento Priority Programador de tareas
topic_type:
- apiref
api_name:
- Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecda59ecbbe23550363fb30706d73bca54fcd925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422033"
---
# <a name="priority-settingstype-element"></a><span data-ttu-id="42a03-104">Elemento Priority (settingsType)</span><span class="sxs-lookup"><span data-stu-id="42a03-104">Priority (settingsType) Element</span></span>

<span data-ttu-id="42a03-105">Especifica el nivel de prioridad de la tarea.</span><span class="sxs-lookup"><span data-stu-id="42a03-105">Specifies the priority level for the task.</span></span>

``` syntax
<xs:element name="Priority"
    type="priorityType"
    default="7"
    minOccurs="0"
 />
```

<span data-ttu-id="42a03-106">El elemento de **prioridad** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="42a03-106">The **Priority** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="42a03-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="42a03-107">Parent element</span></span>



| <span data-ttu-id="42a03-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="42a03-108">Element</span></span>                                                           | <span data-ttu-id="42a03-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="42a03-109">Derived from</span></span>                                                         | <span data-ttu-id="42a03-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="42a03-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="42a03-111">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="42a03-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="42a03-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="42a03-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="42a03-113">Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="42a03-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="42a03-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42a03-114">Remarks</span></span>

<span data-ttu-id="42a03-115">El nivel de prioridad 0 es la prioridad más alta y el nivel de prioridad 10 es la prioridad más baja.</span><span class="sxs-lookup"><span data-stu-id="42a03-115">Priority level 0 is the highest priority, and priority level 10 is the lowest priority.</span></span> <span data-ttu-id="42a03-116">El valor predeterminado es 7.</span><span class="sxs-lookup"><span data-stu-id="42a03-116">The default value is 7.</span></span> <span data-ttu-id="42a03-117">Los valores mínimo y máximo se establecen mediante el tipo simple [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) .</span><span class="sxs-lookup"><span data-stu-id="42a03-117">The minimum and maximum values are set by the [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) simple type.</span></span> <span data-ttu-id="42a03-118">Los niveles de prioridad 7 y 8 se usan para las tareas en segundo plano y los niveles de prioridad 4, 5 y 6 se usan para las tareas interactivas.</span><span class="sxs-lookup"><span data-stu-id="42a03-118">Priority levels 7 and 8 are used for background tasks, and priority levels 4, 5, and 6 are used for interactive tasks.</span></span>

<span data-ttu-id="42a03-119">La acción de la tarea se inicia en un proceso con una prioridad basada en un valor de clase de prioridad.</span><span class="sxs-lookup"><span data-stu-id="42a03-119">The task's action is started in a process with a priority that is based on a Priority Class value.</span></span> <span data-ttu-id="42a03-120">Un valor de nivel de prioridad (prioridad de subproceso) se usa para las acciones de tareas de correo electrónico, el cuadro de mensaje y el controlador COM.</span><span class="sxs-lookup"><span data-stu-id="42a03-120">A Priority Level value (thread priority) is used for COM handler, message box, and email task actions.</span></span> <span data-ttu-id="42a03-121">Para obtener más información sobre la clase de prioridad y los valores de nivel de prioridad, vea [programación de prioridades](/windows/desktop/ProcThread/scheduling-priorities).</span><span class="sxs-lookup"><span data-stu-id="42a03-121">For more information about the Priority Class and Priority Level values, see [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities).</span></span> <span data-ttu-id="42a03-122">En la tabla siguiente se enumeran los valores posibles para el elemento **Priority** y los valores de nivel de prioridad y clase de prioridad correspondientes.</span><span class="sxs-lookup"><span data-stu-id="42a03-122">The following table lists the possible values for the **Priority** element, and the corresponding Priority Class and Priority Level values.</span></span>



| <span data-ttu-id="42a03-123">Prioridad de la tarea</span><span class="sxs-lookup"><span data-stu-id="42a03-123">Task Priority</span></span> | <span data-ttu-id="42a03-124">Priority (clase)</span><span class="sxs-lookup"><span data-stu-id="42a03-124">Priority Class</span></span>                 | <span data-ttu-id="42a03-125">Nivel de prioridad</span><span class="sxs-lookup"><span data-stu-id="42a03-125">Priority Level</span></span>                   |
|---------------|--------------------------------|----------------------------------|
| <span data-ttu-id="42a03-126">0</span><span class="sxs-lookup"><span data-stu-id="42a03-126">0</span></span>             | <span data-ttu-id="42a03-127">\_clase de prioridad en tiempo real \_</span><span class="sxs-lookup"><span data-stu-id="42a03-127">REALTIME\_PRIORITY\_CLASS</span></span>      | <span data-ttu-id="42a03-128">tiempo de prioridad de subproceso \_ \_ \_ crítico</span><span class="sxs-lookup"><span data-stu-id="42a03-128">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span> |
| <span data-ttu-id="42a03-129">1</span><span class="sxs-lookup"><span data-stu-id="42a03-129">1</span></span>             | <span data-ttu-id="42a03-130">\_clase de prioridad alta \_</span><span class="sxs-lookup"><span data-stu-id="42a03-130">HIGH\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="42a03-131">prioridad de subproceso \_ \_ más alta</span><span class="sxs-lookup"><span data-stu-id="42a03-131">THREAD\_PRIORITY\_HIGHEST</span></span>        |
| <span data-ttu-id="42a03-132">2</span><span class="sxs-lookup"><span data-stu-id="42a03-132">2</span></span>             | <span data-ttu-id="42a03-133">POR encima de la \_ \_ clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="42a03-133">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="42a03-134">prioridad de subproceso \_ \_ por encima de lo \_ normal</span><span class="sxs-lookup"><span data-stu-id="42a03-134">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="42a03-135">3</span><span class="sxs-lookup"><span data-stu-id="42a03-135">3</span></span>             | <span data-ttu-id="42a03-136">POR encima de la \_ \_ clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="42a03-136">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="42a03-137">prioridad de subproceso \_ \_ por encima de lo \_ normal</span><span class="sxs-lookup"><span data-stu-id="42a03-137">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="42a03-138">4</span><span class="sxs-lookup"><span data-stu-id="42a03-138">4</span></span>             | <span data-ttu-id="42a03-139">\_clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="42a03-139">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="42a03-140">prioridad de subproceso \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="42a03-140">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="42a03-141">5</span><span class="sxs-lookup"><span data-stu-id="42a03-141">5</span></span>             | <span data-ttu-id="42a03-142">\_clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="42a03-142">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="42a03-143">prioridad de subproceso \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="42a03-143">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="42a03-144">6</span><span class="sxs-lookup"><span data-stu-id="42a03-144">6</span></span>             | <span data-ttu-id="42a03-145">\_clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="42a03-145">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="42a03-146">prioridad de subproceso \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="42a03-146">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="42a03-147">7</span><span class="sxs-lookup"><span data-stu-id="42a03-147">7</span></span>             | <span data-ttu-id="42a03-148">POR debajo de la \_ \_ clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="42a03-148">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="42a03-149">prioridad de subproceso \_ \_ por debajo de lo \_ normal</span><span class="sxs-lookup"><span data-stu-id="42a03-149">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="42a03-150">8</span><span class="sxs-lookup"><span data-stu-id="42a03-150">8</span></span>             | <span data-ttu-id="42a03-151">POR debajo de la \_ \_ clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="42a03-151">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="42a03-152">prioridad de subproceso \_ \_ por debajo de lo \_ normal</span><span class="sxs-lookup"><span data-stu-id="42a03-152">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="42a03-153">9</span><span class="sxs-lookup"><span data-stu-id="42a03-153">9</span></span>             | <span data-ttu-id="42a03-154">\_clase de prioridad INactiva \_</span><span class="sxs-lookup"><span data-stu-id="42a03-154">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="42a03-155">prioridad de subproceso \_ \_ más baja</span><span class="sxs-lookup"><span data-stu-id="42a03-155">THREAD\_PRIORITY\_LOWEST</span></span>         |
| <span data-ttu-id="42a03-156">10</span><span class="sxs-lookup"><span data-stu-id="42a03-156">10</span></span>            | <span data-ttu-id="42a03-157">\_clase de prioridad INactiva \_</span><span class="sxs-lookup"><span data-stu-id="42a03-157">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="42a03-158">prioridad de subproceso \_ \_ inactiva</span><span class="sxs-lookup"><span data-stu-id="42a03-158">THREAD\_PRIORITY\_IDLE</span></span>           |



 

<span data-ttu-id="42a03-159">Para el desarrollo de C++, vea [**propiedad Priority de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).</span><span class="sxs-lookup"><span data-stu-id="42a03-159">For C++ development, see [**Priority Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).</span></span>

<span data-ttu-id="42a03-160">Para el desarrollo de scripts, vea [**TaskSettings. Priority**](tasksettings-priority.md).</span><span class="sxs-lookup"><span data-stu-id="42a03-160">For script development, see [**TaskSettings.Priority**](tasksettings-priority.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42a03-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42a03-161">Requirements</span></span>



| <span data-ttu-id="42a03-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="42a03-162">Requirement</span></span> | <span data-ttu-id="42a03-163">Value</span><span class="sxs-lookup"><span data-stu-id="42a03-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="42a03-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42a03-164">Minimum supported client</span></span><br/> | <span data-ttu-id="42a03-165">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="42a03-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="42a03-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42a03-166">Minimum supported server</span></span><br/> | <span data-ttu-id="42a03-167">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="42a03-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42a03-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="42a03-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a03-169">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="42a03-169">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

