---
title: Objeto TimeTrigger (Windows. applicationmodel. Background. h)
description: Objeto de scripting que representa un desencadenador que inicia una tarea en una fecha y hora específicas.
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- Programador de tareas de tiempo de desencadenador, objeto
- Objeto TimeTrigger Programador de tareas
- Programador de tareas de objeto TimeTrigger, descrito
topic_type:
- apiref
api_name:
- TimeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8403b93e1c5292ade9f6f402b7e41994339140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359774"
---
# <a name="timetrigger-object"></a><span data-ttu-id="44093-106">Objeto TimeTrigger</span><span class="sxs-lookup"><span data-stu-id="44093-106">TimeTrigger object</span></span>

<span data-ttu-id="44093-107">Objeto de scripting que representa un desencadenador que inicia una tarea en una fecha y hora específicas.</span><span class="sxs-lookup"><span data-stu-id="44093-107">Scripting object that represents a trigger that starts a task at a specific date and time.</span></span>

## <a name="members"></a><span data-ttu-id="44093-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="44093-108">Members</span></span>

<span data-ttu-id="44093-109">El objeto **TimeTrigger** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="44093-109">The **TimeTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="44093-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="44093-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44093-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="44093-111">Properties</span></span>

<span data-ttu-id="44093-112">El objeto **TimeTrigger** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="44093-112">The **TimeTrigger** object has these properties.</span></span>



| <span data-ttu-id="44093-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="44093-113">Property</span></span>                                                            | <span data-ttu-id="44093-114">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="44093-114">Access type</span></span>           | <span data-ttu-id="44093-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="44093-115">Description</span></span>                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44093-116">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="44093-116">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="44093-117">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="44093-117">Read/write</span></span><br/> | <span data-ttu-id="44093-118">Heredado del [**desencadenador**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="44093-118">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="44093-119">Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="44093-119">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="44093-120">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="44093-120">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="44093-121">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="44093-121">Read/write</span></span><br/> | <span data-ttu-id="44093-122">Heredado del [**desencadenador**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="44093-122">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="44093-123">Obtiene o establece la fecha y hora en que se desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="44093-123">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="44093-124">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="44093-124">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="44093-125">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="44093-125">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="44093-126">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="44093-126">Read/write</span></span><br/> | <span data-ttu-id="44093-127">Heredado del [**desencadenador**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="44093-127">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="44093-128">Obtiene o establece la cantidad máxima de tiempo que puede ejecutarse la tarea iniciada por el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="44093-128">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="44093-129">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="44093-129">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="44093-130">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="44093-130">Read/write</span></span><br/> | <span data-ttu-id="44093-131">Heredado del [**desencadenador**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="44093-131">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="44093-132">Obtiene o establece el identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="44093-132">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="44093-133">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="44093-133">**RandomDelay**</span></span>](dailytrigger-randomdelay.md)<br/>          | <span data-ttu-id="44093-134">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="44093-134">Read/write</span></span><br/> | <span data-ttu-id="44093-135">Obtiene o establece un tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="44093-135">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                    |
| [<span data-ttu-id="44093-136">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="44093-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="44093-137">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="44093-137">Read/write</span></span><br/> | <span data-ttu-id="44093-138">Heredado del [**desencadenador**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="44093-138">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="44093-139">Obtiene o establece la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="44093-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="44093-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="44093-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="44093-141">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="44093-141">Read/write</span></span><br/> | <span data-ttu-id="44093-142">Heredado del [**desencadenador**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="44093-142">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="44093-143">Obtiene o establece la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="44093-143">Gets or sets the date and time when the trigger is activated.</span></span> <span data-ttu-id="44093-144">Este elemento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="44093-144">This element is required.</span></span><br/>                                    |
| [<span data-ttu-id="44093-145">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="44093-145">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="44093-146">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="44093-146">Read-only</span></span><br/>  | <span data-ttu-id="44093-147">Heredado del [**desencadenador**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="44093-147">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="44093-148">Obtiene el tipo del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="44093-148">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="44093-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44093-149">Remarks</span></span>

<span data-ttu-id="44093-150">El elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores de tiempo y calendario ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) y [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span><span class="sxs-lookup"><span data-stu-id="44093-150">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) and [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="44093-151">Al leer o escribir XML para una tarea, se especifica un desencadenador inactivo mediante el elemento [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) del esquema programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="44093-151">When reading or writing XML for a task, an idle trigger is specified using the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="44093-152">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="44093-152">Examples</span></span>

<span data-ttu-id="44093-153">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="44093-153">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44093-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44093-154">Requirements</span></span>



| <span data-ttu-id="44093-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="44093-155">Requirement</span></span> | <span data-ttu-id="44093-156">Value</span><span class="sxs-lookup"><span data-stu-id="44093-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44093-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44093-157">Minimum supported client</span></span><br/> | <span data-ttu-id="44093-158">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="44093-158">Windows Vista \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="44093-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44093-159">Minimum supported server</span></span><br/> | <span data-ttu-id="44093-160">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="44093-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="44093-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44093-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="44093-162"><dt>Windows. applicationmodel. Background. h</dt></span><span class="sxs-lookup"><span data-stu-id="44093-162"><dt>Windows.applicationmodel.background.h</dt></span></span> </dl> |
| <span data-ttu-id="44093-163">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="44093-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="44093-164"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="44093-164"><dt>Taskschd.tlb</dt></span></span> </dl>                          |
| <span data-ttu-id="44093-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44093-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44093-166"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44093-166"><dt>Taskschd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="44093-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="44093-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44093-168">**Activado**</span><span class="sxs-lookup"><span data-stu-id="44093-168">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="44093-169">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="44093-169">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="44093-170">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="44093-170">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





