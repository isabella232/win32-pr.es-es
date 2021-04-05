---
title: Objeto MonthlyTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea basada en una programación mensual.
ms.assetid: d73715cb-a52e-4daf-930f-e94fbe28881e
keywords:
- Programador de tareas de desencadenador mensual, objeto
- Objeto MonthlyTrigger Programador de tareas
- Programador de tareas de objeto MonthlyTrigger, descrito
topic_type:
- apiref
api_name:
- MonthlyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce433f626fbe45e209f881c00787495cc6343bc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802563"
---
# <a name="monthlytrigger-object"></a><span data-ttu-id="0352f-106">Objeto MonthlyTrigger</span><span class="sxs-lookup"><span data-stu-id="0352f-106">MonthlyTrigger object</span></span>

<span data-ttu-id="0352f-107">Objeto de scripting que representa un desencadenador que inicia una tarea basada en una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="0352f-107">Scripting object that represents a trigger that starts a task based on a monthly schedule.</span></span> <span data-ttu-id="0352f-108">Por ejemplo, la tarea se inicia en días específicos de meses específicos.</span><span class="sxs-lookup"><span data-stu-id="0352f-108">For example, the task starts on specific days of specific months.</span></span>

## <a name="members"></a><span data-ttu-id="0352f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0352f-109">Members</span></span>

<span data-ttu-id="0352f-110">El objeto **MonthlyTrigger** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0352f-110">The **MonthlyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="0352f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0352f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0352f-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0352f-112">Properties</span></span>

<span data-ttu-id="0352f-113">El objeto **MonthlyTrigger** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0352f-113">The **MonthlyTrigger** object has these properties.</span></span>



| <span data-ttu-id="0352f-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0352f-114">Property</span></span>                                                                     | <span data-ttu-id="0352f-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="0352f-115">Access type</span></span>           | <span data-ttu-id="0352f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0352f-116">Description</span></span>                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0352f-117">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="0352f-117">**DaysOfMonth**</span></span>](monthlytrigger-daysofmonth.md)<br/>                 | <span data-ttu-id="0352f-118">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0352f-118">Read/write</span></span><br/> | <span data-ttu-id="0352f-119">Obtiene o establece los días del mes durante los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="0352f-119">Gets or sets the days of the month during which the task runs.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="0352f-120">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="0352f-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                                | <span data-ttu-id="0352f-121">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0352f-121">Read/write</span></span><br/> | <span data-ttu-id="0352f-122">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0352f-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0352f-123">Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0352f-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="0352f-124">EndBoundary</span><span class="sxs-lookup"><span data-stu-id="0352f-124">EndBoundary</span></span>](trigger-endboundary.md)<br/>                            | <span data-ttu-id="0352f-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0352f-125">Read/write</span></span><br/> | <span data-ttu-id="0352f-126">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0352f-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0352f-127">Obtiene o establece la fecha y hora en que se desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="0352f-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="0352f-128">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="0352f-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="0352f-129">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="0352f-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/>          | <span data-ttu-id="0352f-130">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0352f-130">Read/write</span></span><br/> | <span data-ttu-id="0352f-131">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0352f-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0352f-132">Obtiene o establece la cantidad máxima de tiempo que puede ejecutarse la tarea iniciada por el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="0352f-132">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="0352f-133">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="0352f-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                         | <span data-ttu-id="0352f-134">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0352f-134">Read/write</span></span><br/> | <span data-ttu-id="0352f-135">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0352f-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0352f-136">Obtiene o establece el identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="0352f-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="0352f-137">**MonthsOfYear**</span><span class="sxs-lookup"><span data-stu-id="0352f-137">**MonthsOfYear**</span></span>](monthlytrigger-monthsofyear.md)<br/>               | <span data-ttu-id="0352f-138">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0352f-138">Read/write</span></span><br/> | <span data-ttu-id="0352f-139">Obtiene o establece los meses del año en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="0352f-139">Gets or sets the months of the year during which the task runs.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="0352f-140">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="0352f-140">**RandomDelay**</span></span>](monthlytrigger-randomdelay.md)<br/>                 | <span data-ttu-id="0352f-141">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0352f-141">Read/write</span></span><br/> | <span data-ttu-id="0352f-142">Obtiene o establece un tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="0352f-142">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="0352f-143">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="0352f-143">**Repetition**</span></span>](trigger-repetition.md)<br/>                          | <span data-ttu-id="0352f-144">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0352f-144">Read/write</span></span><br/> | <span data-ttu-id="0352f-145">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0352f-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0352f-146">Obtiene o establece la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="0352f-146">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="0352f-147">**RunOnLastDayOfMonth**</span><span class="sxs-lookup"><span data-stu-id="0352f-147">**RunOnLastDayOfMonth**</span></span>](monthlytrigger-runonlastdayofmonth.md)<br/> | <span data-ttu-id="0352f-148">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0352f-148">Read/write</span></span><br/> | <span data-ttu-id="0352f-149">Obtiene o establece un valor booleano que indica que la tarea se ejecuta el último día del mes.</span><span class="sxs-lookup"><span data-stu-id="0352f-149">Gets or sets a Boolean value that indicates that the task runs on the last day of the month.</span></span><br/>                                                                                     |
| [<span data-ttu-id="0352f-150">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="0352f-150">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>                    | <span data-ttu-id="0352f-151">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0352f-151">Read/write</span></span><br/> | <span data-ttu-id="0352f-152">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0352f-152">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0352f-153">Obtiene o establece la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="0352f-153">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="0352f-154">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0352f-154">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                     | <span data-ttu-id="0352f-155">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0352f-155">Read-only</span></span><br/>  | <span data-ttu-id="0352f-156">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0352f-156">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0352f-157">Obtiene el tipo del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="0352f-157">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="0352f-158">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0352f-158">Remarks</span></span>

<span data-ttu-id="0352f-159">La hora del día en que se inicia la tarea se establece mediante la propiedad [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="0352f-159">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="0352f-160">Al leer o escribir su propio XML para una tarea, se especifica un desencadenador mensual mediante el elemento [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="0352f-160">When reading or writing your own XML for a task, a monthly trigger is specified using the [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="0352f-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0352f-161">Requirements</span></span>



| <span data-ttu-id="0352f-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="0352f-162">Requirement</span></span> | <span data-ttu-id="0352f-163">Value</span><span class="sxs-lookup"><span data-stu-id="0352f-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0352f-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0352f-164">Minimum supported client</span></span><br/> | <span data-ttu-id="0352f-165">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0352f-165">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0352f-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0352f-166">Minimum supported server</span></span><br/> | <span data-ttu-id="0352f-167">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0352f-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0352f-168">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0352f-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="0352f-169"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0352f-169"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0352f-170">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0352f-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0352f-171"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0352f-171"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0352f-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="0352f-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0352f-173">**Activado**</span><span class="sxs-lookup"><span data-stu-id="0352f-173">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="0352f-174">Objetos Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="0352f-174">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="0352f-175">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="0352f-175">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="0352f-176">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="0352f-176">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="0352f-177">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="0352f-177">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





