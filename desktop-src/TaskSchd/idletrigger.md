---
title: Objeto IdleTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea cuando se produce una condición de inactividad.
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- desencadenador inactivo Programador de tareas, objeto
- Objeto IdleTrigger Programador de tareas
- Programador de tareas de objeto IdleTrigger, descrito
topic_type:
- apiref
api_name:
- IdleTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72288827fec34257bf4f54a152031ef37068790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686192"
---
# <a name="idletrigger-object"></a><span data-ttu-id="79d76-106">Objeto IdleTrigger</span><span class="sxs-lookup"><span data-stu-id="79d76-106">IdleTrigger object</span></span>

<span data-ttu-id="79d76-107">Objeto de scripting que representa un desencadenador que inicia una tarea cuando se produce una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="79d76-107">Scripting object that represents a trigger that starts a task when an idle condition occurs.</span></span> <span data-ttu-id="79d76-108">Para obtener información sobre las condiciones de inactividad, consulte [condiciones de inactividad de tareas](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="79d76-108">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

## <a name="members"></a><span data-ttu-id="79d76-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="79d76-109">Members</span></span>

<span data-ttu-id="79d76-110">El objeto **IdleTrigger** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="79d76-110">The **IdleTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="79d76-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79d76-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79d76-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79d76-112">Properties</span></span>

<span data-ttu-id="79d76-113">El objeto **IdleTrigger** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="79d76-113">The **IdleTrigger** object has these properties.</span></span>



| <span data-ttu-id="79d76-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="79d76-114">Property</span></span>                                                            | <span data-ttu-id="79d76-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="79d76-115">Access type</span></span>           | <span data-ttu-id="79d76-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="79d76-116">Description</span></span>                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79d76-117">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="79d76-117">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="79d76-118">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="79d76-118">Read/write</span></span><br/> | <span data-ttu-id="79d76-119">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="79d76-119">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="79d76-120">Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="79d76-120">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="79d76-121">EndBoundary</span><span class="sxs-lookup"><span data-stu-id="79d76-121">EndBoundary</span></span>](trigger-endboundary.md)<br/>                   | <span data-ttu-id="79d76-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="79d76-122">Read/write</span></span><br/> | <span data-ttu-id="79d76-123">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="79d76-123">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="79d76-124">Obtiene o establece la fecha y hora en que se desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="79d76-124">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="79d76-125">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="79d76-125">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="79d76-126">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="79d76-126">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="79d76-127">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="79d76-127">Read/write</span></span><br/> | <span data-ttu-id="79d76-128">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="79d76-128">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="79d76-129">Obtiene o establece la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="79d76-129">Gets or sets the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                                 |
| [<span data-ttu-id="79d76-130">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="79d76-130">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="79d76-131">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="79d76-131">Read/write</span></span><br/> | <span data-ttu-id="79d76-132">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="79d76-132">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="79d76-133">Obtiene o establece el identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="79d76-133">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="79d76-134">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="79d76-134">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="79d76-135">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="79d76-135">Read/write</span></span><br/> | <span data-ttu-id="79d76-136">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="79d76-136">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="79d76-137">Obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="79d76-137">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="79d76-138">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="79d76-138">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="79d76-139">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="79d76-139">Read/write</span></span><br/> | <span data-ttu-id="79d76-140">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="79d76-140">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="79d76-141">Obtiene o establece la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="79d76-141">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="79d76-142">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="79d76-142">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="79d76-143">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="79d76-143">Read-only</span></span><br/>  | <span data-ttu-id="79d76-144">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="79d76-144">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="79d76-145">Obtiene el tipo del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="79d76-145">Gets the type of the trigger.</span></span><br/>                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="79d76-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79d76-146">Remarks</span></span>

<span data-ttu-id="79d76-147">Un desencadenador inactivo solo desencadenará una acción de tarea si el equipo entra en un estado de inactividad después del límite de inicio del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="79d76-147">An idle trigger will only trigger a task action if the computer goes into an idle state after the start boundary of the trigger.</span></span>

<span data-ttu-id="79d76-148">Al leer o escribir XML para una tarea, se especifica un desencadenador inactivo mediante el elemento [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) del esquema programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="79d76-148">When reading or writing XML for a task, an idle trigger is specified using the [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="79d76-149">Si una tarea se desencadena mediante un desencadenador inactivo, se omite la propiedad [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="79d76-149">If a task is triggered by an idle trigger, then the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property is ignored.</span></span>

<span data-ttu-id="79d76-150">Si la instancia inicial de una tarea con un desencadenador idle todavía se está ejecutando, la tarea solo se inicia una vez sin repeticiones, aunque se hayan definido varias repeticiones en la propiedad [**repeticiones**](trigger-repetition.md) .</span><span class="sxs-lookup"><span data-stu-id="79d76-150">If the initial instance of a task with an idle trigger is still running, then the task is only launched once with no repetitions, even if multiple repetition is defined in the [**Repetition**](trigger-repetition.md) property.</span></span> <span data-ttu-id="79d76-151">Este comportamiento no se produce si la tarea se detiene por sí misma.</span><span class="sxs-lookup"><span data-stu-id="79d76-151">This behavior does not occur if the task stops by itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="79d76-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79d76-152">Requirements</span></span>



| <span data-ttu-id="79d76-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="79d76-153">Requirement</span></span> | <span data-ttu-id="79d76-154">Value</span><span class="sxs-lookup"><span data-stu-id="79d76-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79d76-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79d76-155">Minimum supported client</span></span><br/> | <span data-ttu-id="79d76-156">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="79d76-156">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="79d76-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79d76-157">Minimum supported server</span></span><br/> | <span data-ttu-id="79d76-158">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="79d76-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="79d76-159">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="79d76-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="79d76-160"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="79d76-160"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="79d76-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79d76-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79d76-162"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79d76-162"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79d76-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="79d76-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79d76-164">**Activado**</span><span class="sxs-lookup"><span data-stu-id="79d76-164">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="79d76-165">Objetos Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="79d76-165">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="79d76-166">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="79d76-166">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





