---
title: Objeto MonthlyDOWTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea en una programación mensual de día de la semana.
ms.assetid: 18607189-295f-4f7d-bf72-f0ac8d5067cf
keywords:
- Programador de tareas de desencadenador de DOW mensual, objeto
- Objeto MonthlyDOWTrigger Programador de tareas
- Programador de tareas de objeto MonthlyDOWTrigger, descrito
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7e43925c6ebe27933a39fe5e25f37ffe6cf72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079162"
---
# <a name="monthlydowtrigger-object"></a><span data-ttu-id="4bb0f-106">Objeto MonthlyDOWTrigger</span><span class="sxs-lookup"><span data-stu-id="4bb0f-106">MonthlyDOWTrigger object</span></span>

<span data-ttu-id="4bb0f-107">Objeto de scripting que representa un desencadenador que inicia una tarea en una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-107">Scripting object that represents a trigger that starts a task on a monthly day-of-week schedule.</span></span> <span data-ttu-id="4bb0f-108">Por ejemplo, la tarea se inicia el primer jueves, de mayo a octubre.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-108">For example, the task starts on every first Thursday, May through October.</span></span>

## <a name="members"></a><span data-ttu-id="4bb0f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4bb0f-109">Members</span></span>

<span data-ttu-id="4bb0f-110">El objeto **MonthlyDOWTrigger** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4bb0f-110">The **MonthlyDOWTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="4bb0f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4bb0f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4bb0f-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4bb0f-112">Properties</span></span>

<span data-ttu-id="4bb0f-113">El objeto **MonthlyDOWTrigger** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-113">The **MonthlyDOWTrigger** object has these properties.</span></span>



| <span data-ttu-id="4bb0f-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4bb0f-114">Property</span></span>                                                                          | <span data-ttu-id="4bb0f-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="4bb0f-115">Access type</span></span>           | <span data-ttu-id="4bb0f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4bb0f-116">Description</span></span>                                                                                                                                                                                 |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4bb0f-117">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="4bb0f-117">**DaysOfWeek**</span></span>](monthlydowtrigger-daysofweek.md)<br/>                     | <span data-ttu-id="4bb0f-118">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4bb0f-118">Read/write</span></span><br/> | <span data-ttu-id="4bb0f-119">Obtiene o establece los días de la semana en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-119">Gets or sets the days of the week during which the task runs.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="4bb0f-120">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="4bb0f-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                                     | <span data-ttu-id="4bb0f-121">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4bb0f-121">Read/write</span></span><br/> | <span data-ttu-id="4bb0f-122">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="4bb0f-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="4bb0f-123">Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="4bb0f-124">EndBoundary</span><span class="sxs-lookup"><span data-stu-id="4bb0f-124">EndBoundary</span></span>](trigger-endboundary.md)<br/>                                 | <span data-ttu-id="4bb0f-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4bb0f-125">Read/write</span></span><br/> | <span data-ttu-id="4bb0f-126">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="4bb0f-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="4bb0f-127">Obtiene o establece la fecha y hora en que se desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="4bb0f-128">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="4bb0f-129">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="4bb0f-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/>               | <span data-ttu-id="4bb0f-130">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4bb0f-130">Read/write</span></span><br/> | <span data-ttu-id="4bb0f-131">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="4bb0f-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="4bb0f-132">Obtiene o establece la cantidad máxima de tiempo que se permite la ejecución de la tarea iniciada por este desencadenador.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-132">Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.</span></span><br/>                          |
| [<span data-ttu-id="4bb0f-133">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="4bb0f-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                              | <span data-ttu-id="4bb0f-134">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4bb0f-134">Read/write</span></span><br/> | <span data-ttu-id="4bb0f-135">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="4bb0f-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="4bb0f-136">Obtiene o establece el identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="4bb0f-137">**MonthsOfYear**</span><span class="sxs-lookup"><span data-stu-id="4bb0f-137">**MonthsOfYear**</span></span>](monthlydowtrigger-monthsofyear.md)<br/>                 | <span data-ttu-id="4bb0f-138">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4bb0f-138">Read/write</span></span><br/> | <span data-ttu-id="4bb0f-139">Obtiene o establece los meses del año en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-139">Gets or sets the months of the year during which the task runs.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="4bb0f-140">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="4bb0f-140">**RandomDelay**</span></span>](monthlydowtrigger-randomdelay.md)<br/>                   | <span data-ttu-id="4bb0f-141">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4bb0f-141">Read/write</span></span><br/> | <span data-ttu-id="4bb0f-142">Obtiene o establece un tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-142">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="4bb0f-143">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="4bb0f-143">**Repetition**</span></span>](trigger-repetition.md)<br/>                               | <span data-ttu-id="4bb0f-144">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4bb0f-144">Read/write</span></span><br/> | <span data-ttu-id="4bb0f-145">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="4bb0f-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="4bb0f-146">Obtiene o establece la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-146">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="4bb0f-147">**RunOnLastWeekOfMonth**</span><span class="sxs-lookup"><span data-stu-id="4bb0f-147">**RunOnLastWeekOfMonth**</span></span>](monthlydowtrigger-runonlastweekofmonth.md)<br/> | <span data-ttu-id="4bb0f-148">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4bb0f-148">Read/write</span></span><br/> | <span data-ttu-id="4bb0f-149">Obtiene o establece un valor booleano que indica que la tarea se ejecuta en la última semana del mes.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-149">Gets or sets a Boolean value that indicates that the task runs on the last week of the month.</span></span><br/>                                                                                    |
| [<span data-ttu-id="4bb0f-150">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="4bb0f-150">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>                         | <span data-ttu-id="4bb0f-151">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4bb0f-151">Read/write</span></span><br/> | <span data-ttu-id="4bb0f-152">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="4bb0f-152">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="4bb0f-153">Obtiene o establece la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-153">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="4bb0f-154">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4bb0f-154">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                          | <span data-ttu-id="4bb0f-155">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4bb0f-155">Read-only</span></span><br/>  | <span data-ttu-id="4bb0f-156">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="4bb0f-156">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="4bb0f-157">Obtiene el tipo del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-157">Gets the type of the trigger.</span></span><br/>                                                                                              |
| [<span data-ttu-id="4bb0f-158">**WeeksOfMonth**</span><span class="sxs-lookup"><span data-stu-id="4bb0f-158">**WeeksOfMonth**</span></span>](monthlydowtrigger-weeksofmonth.md)<br/>                 | <span data-ttu-id="4bb0f-159">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4bb0f-159">Read/write</span></span><br/> | <span data-ttu-id="4bb0f-160">Obtiene o establece las semanas del mes en las que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-160">Gets or sets the weeks of the month during which the task runs.</span></span><br/>                                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="4bb0f-161">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bb0f-161">Remarks</span></span>

<span data-ttu-id="4bb0f-162">La hora del día en que se inicia la tarea se establece mediante la propiedad [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="4bb0f-162">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="4bb0f-163">Al leer o escribir XML para una tarea, se especifica un desencadenador de día de la semana mensual mediante el elemento [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-163">When reading or writing XML for a task, a monthly day-of-week trigger is specified using the [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bb0f-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bb0f-164">Requirements</span></span>



| <span data-ttu-id="4bb0f-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bb0f-165">Requirement</span></span> | <span data-ttu-id="4bb0f-166">Value</span><span class="sxs-lookup"><span data-stu-id="4bb0f-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb0f-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bb0f-167">Minimum supported client</span></span><br/> | <span data-ttu-id="4bb0f-168">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4bb0f-168">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4bb0f-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bb0f-169">Minimum supported server</span></span><br/> | <span data-ttu-id="4bb0f-170">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4bb0f-170">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4bb0f-171">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4bb0f-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="4bb0f-172"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4bb0f-172"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4bb0f-173">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4bb0f-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bb0f-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bb0f-174"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bb0f-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bb0f-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bb0f-176">**Activado**</span><span class="sxs-lookup"><span data-stu-id="4bb0f-176">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="4bb0f-177">Objetos Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="4bb0f-177">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="4bb0f-178">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="4bb0f-178">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="4bb0f-179">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="4bb0f-179">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="4bb0f-180">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="4bb0f-180">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





