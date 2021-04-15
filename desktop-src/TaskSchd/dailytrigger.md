---
title: Objeto DailyTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea en función de una programación diaria.
ms.assetid: f03f53a0-0060-4793-96c1-b47a96852579
keywords:
- Programador de tareas de desencadenador diario, objeto
- Objeto DailyTrigger Programador de tareas
- Programador de tareas de objeto DailyTrigger, descrito
topic_type:
- apiref
api_name:
- DailyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22203ecf7a421f07ccb823745e6619e05f84f550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489874"
---
# <a name="dailytrigger-object"></a><span data-ttu-id="50337-106">Objeto DailyTrigger</span><span class="sxs-lookup"><span data-stu-id="50337-106">DailyTrigger object</span></span>

<span data-ttu-id="50337-107">Objeto de scripting que representa un desencadenador que inicia una tarea en función de una programación diaria.</span><span class="sxs-lookup"><span data-stu-id="50337-107">Scripting object that represents a trigger that starts a task based on a daily schedule.</span></span>

## <a name="members"></a><span data-ttu-id="50337-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="50337-108">Members</span></span>

<span data-ttu-id="50337-109">El objeto **DailyTrigger** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="50337-109">The **DailyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="50337-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="50337-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50337-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="50337-111">Properties</span></span>

<span data-ttu-id="50337-112">El objeto **DailyTrigger** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="50337-112">The **DailyTrigger** object has these properties.</span></span>



| <span data-ttu-id="50337-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="50337-113">Property</span></span>                                                            | <span data-ttu-id="50337-114">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="50337-114">Access type</span></span>           | <span data-ttu-id="50337-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="50337-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50337-116">**DaysInterval**</span><span class="sxs-lookup"><span data-stu-id="50337-116">**DaysInterval**</span></span>](dailytrigger-daysinterval.md)<br/>        | <span data-ttu-id="50337-117">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="50337-117">Read/write</span></span><br/> | <span data-ttu-id="50337-118">Obtiene o establece el intervalo entre los días de la programación.</span><span class="sxs-lookup"><span data-stu-id="50337-118">Gets or sets the interval between the days in the schedule.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="50337-119">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="50337-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="50337-120">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="50337-120">Read/write</span></span><br/> | <span data-ttu-id="50337-121">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="50337-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="50337-122">Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="50337-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="50337-123">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="50337-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="50337-124">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="50337-124">Read/write</span></span><br/> | <span data-ttu-id="50337-125">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="50337-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="50337-126">Obtiene o establece la fecha y hora en que se desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="50337-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="50337-127">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="50337-127">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="50337-128">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="50337-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="50337-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="50337-129">Read/write</span></span><br/> | <span data-ttu-id="50337-130">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="50337-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="50337-131">Obtiene o establece la cantidad máxima de tiempo que puede ejecutarse la tarea iniciada por el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="50337-131">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="50337-132">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="50337-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="50337-133">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="50337-133">Read/write</span></span><br/> | <span data-ttu-id="50337-134">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="50337-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="50337-135">Obtiene o establece el identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="50337-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="50337-136">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="50337-136">**RandomDelay**</span></span>](dailytrigger-randomdelay.md)<br/>          | <span data-ttu-id="50337-137">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="50337-137">Read/write</span></span><br/> | <span data-ttu-id="50337-138">Obtiene o establece un tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="50337-138">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="50337-139">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="50337-139">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="50337-140">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="50337-140">Read/write</span></span><br/> | <span data-ttu-id="50337-141">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="50337-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="50337-142">Obtiene o establece la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="50337-142">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="50337-143">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="50337-143">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="50337-144">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="50337-144">Read/write</span></span><br/> | <span data-ttu-id="50337-145">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="50337-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="50337-146">Obtiene o establece la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="50337-146">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="50337-147">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="50337-147">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="50337-148">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="50337-148">Read-only</span></span><br/>  | <span data-ttu-id="50337-149">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="50337-149">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="50337-150">Obtiene el tipo del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="50337-150">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="50337-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50337-151">Remarks</span></span>

<span data-ttu-id="50337-152">La hora del día en que se inicia la tarea se establece mediante la propiedad [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="50337-152">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="50337-153">Un intervalo de 1 genera una programación diaria.</span><span class="sxs-lookup"><span data-stu-id="50337-153">An interval of 1 produces a daily schedule.</span></span> <span data-ttu-id="50337-154">Un intervalo de 2 genera una programación de cada día, etc.</span><span class="sxs-lookup"><span data-stu-id="50337-154">An interval of 2 produces an every other day schedule and so on.</span></span>

<span data-ttu-id="50337-155">Al leer o escribir su propio XML para una tarea, se especifica un desencadenador diario mediante el elemento [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="50337-155">When reading or writing your own XML for a task, a daily trigger is specified using the [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="50337-156">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="50337-156">Examples</span></span>

<span data-ttu-id="50337-157">Para obtener más información y un ejemplo de código para este objeto de scripting, vea [ejemplo de desencadenador diario (scripting)](daily-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="50337-157">For more information and a code example for this scripting object, see [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50337-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50337-158">Requirements</span></span>



| <span data-ttu-id="50337-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="50337-159">Requirement</span></span> | <span data-ttu-id="50337-160">Value</span><span class="sxs-lookup"><span data-stu-id="50337-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50337-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50337-161">Minimum supported client</span></span><br/> | <span data-ttu-id="50337-162">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="50337-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="50337-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50337-163">Minimum supported server</span></span><br/> | <span data-ttu-id="50337-164">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="50337-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="50337-165">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="50337-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="50337-166"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="50337-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="50337-167">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="50337-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50337-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50337-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50337-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="50337-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50337-170">**Activado**</span><span class="sxs-lookup"><span data-stu-id="50337-170">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="50337-171">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="50337-171">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="50337-172">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="50337-172">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





