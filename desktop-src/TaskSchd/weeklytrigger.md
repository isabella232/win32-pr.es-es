---
title: Objeto WeeklyTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea basada en una programación semanal.
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- Programador de tareas de desencadenador semanal, objeto
- Objeto WeeklyTrigger Programador de tareas
- Programador de tareas de objeto WeeklyTrigger, descrito
topic_type:
- apiref
api_name:
- WeeklyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58dec9172d38b53f779f44a048b39bc709dbd54f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804039"
---
# <a name="weeklytrigger-object"></a><span data-ttu-id="673a0-106">Objeto WeeklyTrigger</span><span class="sxs-lookup"><span data-stu-id="673a0-106">WeeklyTrigger object</span></span>

<span data-ttu-id="673a0-107">Objeto de scripting que representa un desencadenador que inicia una tarea basada en una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="673a0-107">Scripting object that represents a trigger that starts a task based on a weekly schedule.</span></span> <span data-ttu-id="673a0-108">Por ejemplo, la tarea comienza a las 8:00 A.M.</span><span class="sxs-lookup"><span data-stu-id="673a0-108">For example, the task starts at 8:00 A.M.</span></span> <span data-ttu-id="673a0-109">en un día concreto de la semana cada semana o cada dos semanas.</span><span class="sxs-lookup"><span data-stu-id="673a0-109">on a specific day of the week every week or every other week.</span></span>

## <a name="members"></a><span data-ttu-id="673a0-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="673a0-110">Members</span></span>

<span data-ttu-id="673a0-111">El objeto **WeeklyTrigger** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="673a0-111">The **WeeklyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="673a0-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="673a0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="673a0-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="673a0-113">Properties</span></span>

<span data-ttu-id="673a0-114">El objeto **WeeklyTrigger** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="673a0-114">The **WeeklyTrigger** object has these properties.</span></span>



| <span data-ttu-id="673a0-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="673a0-115">Property</span></span>                                                            | <span data-ttu-id="673a0-116">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="673a0-116">Access type</span></span>           | <span data-ttu-id="673a0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="673a0-117">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="673a0-118">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="673a0-118">**DaysOfWeek**</span></span>](weeklytrigger-daysofweek.md)<br/>           | <span data-ttu-id="673a0-119">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="673a0-119">Read/write</span></span><br/> | <span data-ttu-id="673a0-120">Obtiene o establece los días de la semana en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="673a0-120">Gets or sets the days of the week on which the task runs.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="673a0-121">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="673a0-121">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="673a0-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="673a0-122">Read/write</span></span><br/> | <span data-ttu-id="673a0-123">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="673a0-123">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="673a0-124">Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="673a0-124">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="673a0-125">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="673a0-125">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="673a0-126">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="673a0-126">Read/write</span></span><br/> | <span data-ttu-id="673a0-127">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="673a0-127">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="673a0-128">Obtiene o establece la fecha y hora en que se desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="673a0-128">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="673a0-129">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="673a0-129">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="673a0-130">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="673a0-130">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="673a0-131">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="673a0-131">Read/write</span></span><br/> | <span data-ttu-id="673a0-132">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="673a0-132">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="673a0-133">Obtiene o establece la cantidad máxima de tiempo que puede ejecutarse la tarea iniciada por el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="673a0-133">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="673a0-134">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="673a0-134">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="673a0-135">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="673a0-135">Read/write</span></span><br/> | <span data-ttu-id="673a0-136">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="673a0-136">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="673a0-137">Obtiene o establece el identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="673a0-137">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="673a0-138">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="673a0-138">**RandomDelay**</span></span>](weeklytrigger-randomdelay.md)<br/>         | <span data-ttu-id="673a0-139">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="673a0-139">Read/write</span></span><br/> | <span data-ttu-id="673a0-140">Obtiene o establece un tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="673a0-140">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="673a0-141">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="673a0-141">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="673a0-142">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="673a0-142">Read/write</span></span><br/> | <span data-ttu-id="673a0-143">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="673a0-143">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="673a0-144">Obtiene o establece la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="673a0-144">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="673a0-145">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="673a0-145">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="673a0-146">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="673a0-146">Read/write</span></span><br/> | <span data-ttu-id="673a0-147">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="673a0-147">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="673a0-148">Obtiene o establece la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="673a0-148">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="673a0-149">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="673a0-149">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="673a0-150">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="673a0-150">Read-only</span></span><br/>  | <span data-ttu-id="673a0-151">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="673a0-151">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="673a0-152">Obtiene el tipo del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="673a0-152">Gets the type of the trigger.</span></span><br/>                                                                                              |
| [<span data-ttu-id="673a0-153">**WeeksInterval**</span><span class="sxs-lookup"><span data-stu-id="673a0-153">**WeeksInterval**</span></span>](weeklytrigger-weeksinterval.md)<br/>     | <span data-ttu-id="673a0-154">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="673a0-154">Read/write</span></span><br/> | <span data-ttu-id="673a0-155">Obtiene o establece el intervalo entre las semanas de la programación.</span><span class="sxs-lookup"><span data-stu-id="673a0-155">Gets or sets the interval between the weeks in the schedule.</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="673a0-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="673a0-156">Remarks</span></span>

<span data-ttu-id="673a0-157">La hora del día en que se inicia la tarea se establece mediante la propiedad [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="673a0-157">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="673a0-158">Al leer o escribir su propio XML para una tarea, se especifica un desencadenador semanal mediante el elemento [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="673a0-158">When reading or writing your own XML for a task, a weekly trigger is specified using the [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="673a0-159">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="673a0-159">Examples</span></span>

<span data-ttu-id="673a0-160">Para obtener más información y un ejemplo de código para este objeto de scripting, vea [ejemplo de desencadenador semanal (scripting)](weekly-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="673a0-160">For more information and a code example for this scripting object, see [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="673a0-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="673a0-161">Requirements</span></span>



| <span data-ttu-id="673a0-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="673a0-162">Requirement</span></span> | <span data-ttu-id="673a0-163">Value</span><span class="sxs-lookup"><span data-stu-id="673a0-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="673a0-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="673a0-164">Minimum supported client</span></span><br/> | <span data-ttu-id="673a0-165">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="673a0-165">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="673a0-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="673a0-166">Minimum supported server</span></span><br/> | <span data-ttu-id="673a0-167">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="673a0-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="673a0-168">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="673a0-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="673a0-169"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="673a0-169"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="673a0-170">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="673a0-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="673a0-171"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="673a0-171"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="673a0-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="673a0-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="673a0-173">**Activado**</span><span class="sxs-lookup"><span data-stu-id="673a0-173">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="673a0-174">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="673a0-174">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="673a0-175">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="673a0-175">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





