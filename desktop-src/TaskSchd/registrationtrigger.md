---
title: Objeto RegistrationTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea cuando la tarea se registra o se actualiza.
ms.assetid: 430ef3e0-9409-49ff-8ffb-31833938d8b2
keywords:
- Programador de tareas de desencadenador de registro, objeto
- Objeto RegistrationTrigger Programador de tareas
- Programador de tareas de objeto RegistrationTrigger, descrito
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08bf84fa92b1736b2989c1920abb8f0af2c0b97c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534467"
---
# <a name="registrationtrigger-object"></a><span data-ttu-id="7a310-106">Objeto RegistrationTrigger</span><span class="sxs-lookup"><span data-stu-id="7a310-106">RegistrationTrigger object</span></span>

<span data-ttu-id="7a310-107">Objeto de scripting que representa un desencadenador que inicia una tarea cuando la tarea se registra o se actualiza.</span><span class="sxs-lookup"><span data-stu-id="7a310-107">Scripting object that represents a trigger that starts a task when the task is registered or updated.</span></span>

## <a name="members"></a><span data-ttu-id="7a310-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7a310-108">Members</span></span>

<span data-ttu-id="7a310-109">El objeto **RegistrationTrigger** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7a310-109">The **RegistrationTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="7a310-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a310-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a310-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a310-111">Properties</span></span>

<span data-ttu-id="7a310-112">El objeto **RegistrationTrigger** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7a310-112">The **RegistrationTrigger** object has these properties.</span></span>



| <span data-ttu-id="7a310-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7a310-113">Property</span></span>                                                            | <span data-ttu-id="7a310-114">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="7a310-114">Access type</span></span>           | <span data-ttu-id="7a310-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a310-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a310-116">**Delay**</span><span class="sxs-lookup"><span data-stu-id="7a310-116">**Delay**</span></span>](registrationtrigger-delay.md)<br/>               | <span data-ttu-id="7a310-117">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7a310-117">Read/write</span></span><br/> | <span data-ttu-id="7a310-118">Obtiene o establece la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="7a310-118">Gets or sets the amount of time between when the task is registered and when the task is started.</span></span><br/>                                                                                |
| [<span data-ttu-id="7a310-119">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="7a310-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="7a310-120">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7a310-120">Read/write</span></span><br/> | <span data-ttu-id="7a310-121">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="7a310-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="7a310-122">Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="7a310-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="7a310-123">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="7a310-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="7a310-124">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7a310-124">Read/write</span></span><br/> | <span data-ttu-id="7a310-125">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="7a310-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="7a310-126">Obtiene o establece la fecha y hora en que se desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="7a310-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="7a310-127">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="7a310-127">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="7a310-128">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="7a310-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="7a310-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7a310-129">Read/write</span></span><br/> | <span data-ttu-id="7a310-130">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="7a310-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="7a310-131">Obtiene o establece la cantidad máxima de tiempo que puede ejecutarse la tarea iniciada por el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="7a310-131">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="7a310-132">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="7a310-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="7a310-133">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7a310-133">Read/write</span></span><br/> | <span data-ttu-id="7a310-134">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="7a310-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="7a310-135">Obtiene o establece el identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="7a310-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="7a310-136">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="7a310-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="7a310-137">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7a310-137">Read/write</span></span><br/> | <span data-ttu-id="7a310-138">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="7a310-138">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="7a310-139">Obtiene o establece la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="7a310-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="7a310-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="7a310-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="7a310-141">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7a310-141">Read/write</span></span><br/> | <span data-ttu-id="7a310-142">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="7a310-142">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="7a310-143">Obtiene o establece la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="7a310-143">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="7a310-144">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7a310-144">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="7a310-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a310-145">Read-only</span></span><br/>  | <span data-ttu-id="7a310-146">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="7a310-146">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="7a310-147">Obtiene el tipo del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="7a310-147">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="7a310-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a310-148">Remarks</span></span>

<span data-ttu-id="7a310-149">Al crear su propio XML para una tarea, se especifica un desencadenador de registro mediante el elemento [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="7a310-149">When creating your own XML for a task, a registration trigger is specified using the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="7a310-150">Si se registra una tarea con un desencadenador de registro retrasado y el equipo en el que se ha registrado la tarea se cierra o se reinicia durante el retraso, antes de que se ejecute la tarea, la tarea no se ejecutará y se perderá el retraso.</span><span class="sxs-lookup"><span data-stu-id="7a310-150">If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during the delay, before the task runs, then the task will not run and the delay will be lost.</span></span>

## <a name="examples"></a><span data-ttu-id="7a310-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7a310-151">Examples</span></span>

<span data-ttu-id="7a310-152">Para obtener más información y un ejemplo de código para este objeto de scripting, vea [ejemplo de desencadenador de registro (scripting)](registration-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="7a310-152">For more information and a code example for this scripting object, see [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a310-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a310-153">Requirements</span></span>



| <span data-ttu-id="7a310-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a310-154">Requirement</span></span> | <span data-ttu-id="7a310-155">Value</span><span class="sxs-lookup"><span data-stu-id="7a310-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a310-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a310-156">Minimum supported client</span></span><br/> | <span data-ttu-id="7a310-157">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7a310-157">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7a310-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a310-158">Minimum supported server</span></span><br/> | <span data-ttu-id="7a310-159">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7a310-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7a310-160">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7a310-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a310-161"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7a310-161"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7a310-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7a310-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a310-163"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a310-163"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a310-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a310-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a310-165">**Activado**</span><span class="sxs-lookup"><span data-stu-id="7a310-165">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="7a310-166">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="7a310-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="7a310-167">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="7a310-167">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





