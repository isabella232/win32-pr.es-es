---
title: Objeto BootTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea cuando se inicia el sistema.
ms.assetid: 9d5a7cf6-2e1d-44ae-bb45-66424770d61b
keywords:
- Programador de tareas de desencadenador de arranque, objeto
- Objeto BootTrigger Programador de tareas
- Programador de tareas de objeto BootTrigger, descrito
topic_type:
- apiref
api_name:
- BootTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 346a4bc7b20606f59c26b131590b92593d40d07e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493133"
---
# <a name="boottrigger-object"></a><span data-ttu-id="95463-106">Objeto BootTrigger</span><span class="sxs-lookup"><span data-stu-id="95463-106">BootTrigger object</span></span>

<span data-ttu-id="95463-107">Objeto de scripting que representa un desencadenador que inicia una tarea cuando se inicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="95463-107">Scripting object that represents a trigger that starts a task when the system is booted.</span></span>

## <a name="members"></a><span data-ttu-id="95463-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="95463-108">Members</span></span>

<span data-ttu-id="95463-109">El objeto **BootTrigger** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="95463-109">The **BootTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="95463-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95463-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95463-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95463-111">Properties</span></span>

<span data-ttu-id="95463-112">El objeto **BootTrigger** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="95463-112">The **BootTrigger** object has these properties.</span></span>



| <span data-ttu-id="95463-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="95463-113">Property</span></span>                                                            | <span data-ttu-id="95463-114">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="95463-114">Access type</span></span>           | <span data-ttu-id="95463-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="95463-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95463-116">**Delay**</span><span class="sxs-lookup"><span data-stu-id="95463-116">**Delay**</span></span>](boottrigger-delay.md)<br/>                       |                       | <span data-ttu-id="95463-117">Obtiene o establece un valor que indica la cantidad de tiempo entre el momento en el que se arranca el sistema y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="95463-117">Gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.</span></span><br/>                                                           |
| [<span data-ttu-id="95463-118">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="95463-118">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="95463-119">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="95463-119">Read/write</span></span><br/> | <span data-ttu-id="95463-120">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="95463-120">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="95463-121">Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="95463-121">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="95463-122">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="95463-122">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="95463-123">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="95463-123">Read/write</span></span><br/> | <span data-ttu-id="95463-124">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="95463-124">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="95463-125">Obtiene o establece la fecha y hora en que se desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="95463-125">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="95463-126">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="95463-126">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="95463-127">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="95463-127">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="95463-128">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="95463-128">Read/write</span></span><br/> | <span data-ttu-id="95463-129">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="95463-129">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="95463-130">Obtiene o establece la cantidad máxima de tiempo que puede ejecutarse la tarea iniciada por el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="95463-130">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="95463-131">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="95463-131">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="95463-132">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="95463-132">Read/write</span></span><br/> | <span data-ttu-id="95463-133">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="95463-133">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="95463-134">Obtiene o establece el identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="95463-134">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="95463-135">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="95463-135">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="95463-136">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="95463-136">Read/write</span></span><br/> | <span data-ttu-id="95463-137">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="95463-137">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="95463-138">Obtiene o establece la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="95463-138">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="95463-139">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="95463-139">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="95463-140">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="95463-140">Read/write</span></span><br/> | <span data-ttu-id="95463-141">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="95463-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="95463-142">Obtiene o establece la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="95463-142">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="95463-143">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="95463-143">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="95463-144">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="95463-144">Read-only</span></span><br/>  | <span data-ttu-id="95463-145">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="95463-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="95463-146">Obtiene el tipo del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="95463-146">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="95463-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95463-147">Remarks</span></span>

<span data-ttu-id="95463-148">El servicio de Programador de tareas se inicia cuando se inicia el sistema operativo y las tareas de desencadenador de arranque se establecen para iniciarse cuando se inicia el servicio Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="95463-148">The Task Scheduler service is started when the operating system is booted, and boot trigger tasks are set to start when the Task Scheduler service starts.</span></span>

<span data-ttu-id="95463-149">Solo un miembro del grupo administradores puede crear una tarea con un desencadenador de arranque.</span><span class="sxs-lookup"><span data-stu-id="95463-149">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="95463-150">Al crear su propio XML para una tarea, se especifica un desencadenador de arranque mediante el elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="95463-150">When creating your own XML for a task, a boot trigger is specified using the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="95463-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="95463-151">Examples</span></span>

<span data-ttu-id="95463-152">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de arranque (scripting)](boot-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="95463-152">For more information and example code for this scripting object, see [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95463-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95463-153">Requirements</span></span>



| <span data-ttu-id="95463-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="95463-154">Requirement</span></span> | <span data-ttu-id="95463-155">Value</span><span class="sxs-lookup"><span data-stu-id="95463-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95463-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95463-156">Minimum supported client</span></span><br/> | <span data-ttu-id="95463-157">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="95463-157">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="95463-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95463-158">Minimum supported server</span></span><br/> | <span data-ttu-id="95463-159">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="95463-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="95463-160">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="95463-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="95463-161"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="95463-161"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="95463-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95463-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95463-163"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95463-163"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95463-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="95463-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95463-165">**Activado**</span><span class="sxs-lookup"><span data-stu-id="95463-165">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="95463-166">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="95463-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="95463-167">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="95463-167">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





