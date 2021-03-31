---
title: Propiedad TaskSettings. Priority
description: En el caso de scripting, obtiene o establece el nivel de prioridad de la tarea.
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Propiedad Priority Programador de tareas
- Propiedad Priority Programador de tareas, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad Priority
topic_type:
- apiref
api_name:
- TaskSettings.Priority
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282c688d63bb21f2dc0bab43acde7f089fa960b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996027"
---
# <a name="tasksettingspriority-property"></a><span data-ttu-id="85f1e-106">Propiedad TaskSettings. Priority</span><span class="sxs-lookup"><span data-stu-id="85f1e-106">TaskSettings.Priority property</span></span>

<span data-ttu-id="85f1e-107">En el caso de scripting, obtiene o establece el nivel de prioridad de la tarea.</span><span class="sxs-lookup"><span data-stu-id="85f1e-107">For scripting, gets or sets the priority level of the task.</span></span>

<span data-ttu-id="85f1e-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="85f1e-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="85f1e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85f1e-109">Syntax</span></span>


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a><span data-ttu-id="85f1e-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="85f1e-110">Property value</span></span>

<span data-ttu-id="85f1e-111">Nivel de prioridad (0-10) de la tarea.</span><span class="sxs-lookup"><span data-stu-id="85f1e-111">The priority level (0-10) of the task.</span></span> <span data-ttu-id="85f1e-112">El valor predeterminado es 7.</span><span class="sxs-lookup"><span data-stu-id="85f1e-112">The default is 7.</span></span>

## <a name="remarks"></a><span data-ttu-id="85f1e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85f1e-113">Remarks</span></span>

<span data-ttu-id="85f1e-114">El nivel de prioridad 0 es la prioridad más alta y el nivel de prioridad 10 es la prioridad más baja.</span><span class="sxs-lookup"><span data-stu-id="85f1e-114">Priority level 0 is the highest priority, and priority level 10 is the lowest priority.</span></span> <span data-ttu-id="85f1e-115">El valor predeterminado es 7.</span><span class="sxs-lookup"><span data-stu-id="85f1e-115">The default value is 7.</span></span> <span data-ttu-id="85f1e-116">Los niveles de prioridad 7 y 8 se usan para las tareas en segundo plano y los niveles de prioridad 4, 5 y 6 se usan para las tareas interactivas.</span><span class="sxs-lookup"><span data-stu-id="85f1e-116">Priority levels 7 and 8 are used for background tasks, and priority levels 4, 5, and 6 are used for interactive tasks.</span></span>

<span data-ttu-id="85f1e-117">La acción de la tarea se inicia en un proceso con una prioridad basada en un valor de clase de prioridad.</span><span class="sxs-lookup"><span data-stu-id="85f1e-117">The task's action is started in a process with a priority that is based on a Priority Class value.</span></span> <span data-ttu-id="85f1e-118">Un valor de nivel de prioridad (prioridad de subproceso) se usa para las acciones de tareas de correo electrónico, el cuadro de mensaje y el controlador COM.</span><span class="sxs-lookup"><span data-stu-id="85f1e-118">A Priority Level value (thread priority) is used for COM handler, message box, and email task actions.</span></span> <span data-ttu-id="85f1e-119">Para obtener más información sobre la clase de prioridad y los valores de nivel de prioridad, vea [programación de prioridades](/windows/desktop/ProcThread/scheduling-priorities).</span><span class="sxs-lookup"><span data-stu-id="85f1e-119">For more information about the Priority Class and Priority Level values, see [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities).</span></span> <span data-ttu-id="85f1e-120">En la tabla siguiente se enumeran los valores posibles para el parámetro *Priority* y los valores de nivel de prioridad y clase de prioridad correspondientes.</span><span class="sxs-lookup"><span data-stu-id="85f1e-120">The following table lists the possible values for the *priority* parameter, and the corresponding Priority Class and Priority Level values.</span></span>



| <span data-ttu-id="85f1e-121">*Prioridad* de la tarea</span><span class="sxs-lookup"><span data-stu-id="85f1e-121">Task *priority*</span></span> | <span data-ttu-id="85f1e-122">Priority (clase)</span><span class="sxs-lookup"><span data-stu-id="85f1e-122">Priority Class</span></span>                 | <span data-ttu-id="85f1e-123">Nivel de prioridad</span><span class="sxs-lookup"><span data-stu-id="85f1e-123">Priority Level</span></span>                   |
|-----------------|--------------------------------|----------------------------------|
| <span data-ttu-id="85f1e-124">0</span><span class="sxs-lookup"><span data-stu-id="85f1e-124">0</span></span>               | <span data-ttu-id="85f1e-125">\_clase de prioridad en tiempo real \_</span><span class="sxs-lookup"><span data-stu-id="85f1e-125">REALTIME\_PRIORITY\_CLASS</span></span>      | <span data-ttu-id="85f1e-126">tiempo de prioridad de subproceso \_ \_ \_ crítico</span><span class="sxs-lookup"><span data-stu-id="85f1e-126">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span> |
| <span data-ttu-id="85f1e-127">1</span><span class="sxs-lookup"><span data-stu-id="85f1e-127">1</span></span>               | <span data-ttu-id="85f1e-128">\_clase de prioridad alta \_</span><span class="sxs-lookup"><span data-stu-id="85f1e-128">HIGH\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="85f1e-129">prioridad de subproceso \_ \_ más alta</span><span class="sxs-lookup"><span data-stu-id="85f1e-129">THREAD\_PRIORITY\_HIGHEST</span></span>        |
| <span data-ttu-id="85f1e-130">2</span><span class="sxs-lookup"><span data-stu-id="85f1e-130">2</span></span>               | <span data-ttu-id="85f1e-131">POR encima de la \_ \_ clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="85f1e-131">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="85f1e-132">prioridad de subproceso \_ \_ por encima de lo \_ normal</span><span class="sxs-lookup"><span data-stu-id="85f1e-132">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="85f1e-133">3</span><span class="sxs-lookup"><span data-stu-id="85f1e-133">3</span></span>               | <span data-ttu-id="85f1e-134">POR encima de la \_ \_ clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="85f1e-134">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="85f1e-135">prioridad de subproceso \_ \_ por encima de lo \_ normal</span><span class="sxs-lookup"><span data-stu-id="85f1e-135">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="85f1e-136">4</span><span class="sxs-lookup"><span data-stu-id="85f1e-136">4</span></span>               | <span data-ttu-id="85f1e-137">\_clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="85f1e-137">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="85f1e-138">prioridad de subproceso \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="85f1e-138">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="85f1e-139">5</span><span class="sxs-lookup"><span data-stu-id="85f1e-139">5</span></span>               | <span data-ttu-id="85f1e-140">\_clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="85f1e-140">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="85f1e-141">prioridad de subproceso \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="85f1e-141">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="85f1e-142">6</span><span class="sxs-lookup"><span data-stu-id="85f1e-142">6</span></span>               | <span data-ttu-id="85f1e-143">\_clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="85f1e-143">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="85f1e-144">prioridad de subproceso \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="85f1e-144">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="85f1e-145">7</span><span class="sxs-lookup"><span data-stu-id="85f1e-145">7</span></span>               | <span data-ttu-id="85f1e-146">POR debajo de la \_ \_ clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="85f1e-146">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="85f1e-147">prioridad de subproceso \_ \_ por debajo de lo \_ normal</span><span class="sxs-lookup"><span data-stu-id="85f1e-147">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="85f1e-148">8</span><span class="sxs-lookup"><span data-stu-id="85f1e-148">8</span></span>               | <span data-ttu-id="85f1e-149">POR debajo de la \_ \_ clase de prioridad normal \_</span><span class="sxs-lookup"><span data-stu-id="85f1e-149">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="85f1e-150">prioridad de subproceso \_ \_ por debajo de lo \_ normal</span><span class="sxs-lookup"><span data-stu-id="85f1e-150">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="85f1e-151">9</span><span class="sxs-lookup"><span data-stu-id="85f1e-151">9</span></span>               | <span data-ttu-id="85f1e-152">\_clase de prioridad INactiva \_</span><span class="sxs-lookup"><span data-stu-id="85f1e-152">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="85f1e-153">prioridad de subproceso \_ \_ más baja</span><span class="sxs-lookup"><span data-stu-id="85f1e-153">THREAD\_PRIORITY\_LOWEST</span></span>         |
| <span data-ttu-id="85f1e-154">10</span><span class="sxs-lookup"><span data-stu-id="85f1e-154">10</span></span>              | <span data-ttu-id="85f1e-155">\_clase de prioridad INactiva \_</span><span class="sxs-lookup"><span data-stu-id="85f1e-155">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="85f1e-156">prioridad de subproceso \_ \_ inactiva</span><span class="sxs-lookup"><span data-stu-id="85f1e-156">THREAD\_PRIORITY\_IDLE</span></span>           |



 

<span data-ttu-id="85f1e-157">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="85f1e-157">When reading or writing XML for a task, this setting is specified in the [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="85f1e-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85f1e-158">Requirements</span></span>



| <span data-ttu-id="85f1e-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="85f1e-159">Requirement</span></span> | <span data-ttu-id="85f1e-160">Value</span><span class="sxs-lookup"><span data-stu-id="85f1e-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85f1e-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85f1e-161">Minimum supported client</span></span><br/> | <span data-ttu-id="85f1e-162">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="85f1e-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="85f1e-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85f1e-163">Minimum supported server</span></span><br/> | <span data-ttu-id="85f1e-164">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="85f1e-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="85f1e-165">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="85f1e-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="85f1e-166"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="85f1e-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="85f1e-167">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85f1e-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85f1e-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85f1e-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85f1e-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="85f1e-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85f1e-170">**TaskSettings**</span><span class="sxs-lookup"><span data-stu-id="85f1e-170">**TaskSettings**</span></span>](tasksettings.md)
</dt> </dl>

 

