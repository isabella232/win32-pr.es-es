---
title: Objeto SessionStateChangeTrigger
description: Objeto de scripting que desencadena tareas de conexión o desconexión de la consola, conexión remota o desconexión, o notificaciones de bloqueo o desbloqueo de la estación de trabajo.
ms.assetid: ea450b8a-81cc-4d24-b850-78c967dcc5b8
keywords:
- Objeto SessionStateChangeTrigger Programador de tareas
- Programador de tareas de objeto SessionStateChangeTrigger, descrito
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55d41f495c714fe2e1798c79cc4f24b99987a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676651"
---
# <a name="sessionstatechangetrigger-object"></a><span data-ttu-id="d9f92-105">Objeto SessionStateChangeTrigger</span><span class="sxs-lookup"><span data-stu-id="d9f92-105">SessionStateChangeTrigger object</span></span>

<span data-ttu-id="d9f92-106">Objeto de scripting que desencadena tareas de conexión o desconexión de la consola, conexión remota o desconexión, o notificaciones de bloqueo o desbloqueo de la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d9f92-106">Scripting object that triggers tasks for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.</span></span>

## <a name="members"></a><span data-ttu-id="d9f92-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d9f92-107">Members</span></span>

<span data-ttu-id="d9f92-108">El objeto **SessionStateChangeTrigger** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d9f92-108">The **SessionStateChangeTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="d9f92-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9f92-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9f92-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9f92-110">Properties</span></span>

<span data-ttu-id="d9f92-111">El objeto **SessionStateChangeTrigger** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d9f92-111">The **SessionStateChangeTrigger** object has these properties.</span></span>



| <span data-ttu-id="d9f92-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d9f92-112">Property</span></span>                                                                | <span data-ttu-id="d9f92-113">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="d9f92-113">Access type</span></span>           | <span data-ttu-id="d9f92-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9f92-114">Description</span></span>                                                                                                                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9f92-115">**Delay**</span><span class="sxs-lookup"><span data-stu-id="d9f92-115">**Delay**</span></span>](sessionstatechangetrigger-delay.md)<br/>             | <span data-ttu-id="d9f92-116">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d9f92-116">Read/write</span></span><br/> | <span data-ttu-id="d9f92-117">Obtiene o establece un valor que indica cuánto tiempo se produce un retraso antes de que se inicie una tarea después de que se detecte un cambio de estado de sesión Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="d9f92-117">Gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected.</span></span><br/>                                         |
| [<span data-ttu-id="d9f92-118">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="d9f92-118">**Enabled**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled)<br/>                          | <span data-ttu-id="d9f92-119">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d9f92-119">Read/write</span></span><br/> | <span data-ttu-id="d9f92-120">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d9f92-120">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d9f92-121">Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="d9f92-121">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="d9f92-122">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="d9f92-122">**EndBoundary**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary)<br/>                  | <span data-ttu-id="d9f92-123">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d9f92-123">Read/write</span></span><br/> | <span data-ttu-id="d9f92-124">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d9f92-124">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d9f92-125">Obtiene o establece la fecha y hora en que se desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="d9f92-125">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="d9f92-126">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="d9f92-126">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="d9f92-127">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="d9f92-127">**ExecutionTimeLimit**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit)<br/>    | <span data-ttu-id="d9f92-128">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d9f92-128">Read/write</span></span><br/> | <span data-ttu-id="d9f92-129">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d9f92-129">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d9f92-130">Obtiene o establece la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="d9f92-130">Gets or sets the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                                 |
| [<span data-ttu-id="d9f92-131">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="d9f92-131">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                    | <span data-ttu-id="d9f92-132">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d9f92-132">Read/write</span></span><br/> | <span data-ttu-id="d9f92-133">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d9f92-133">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d9f92-134">Obtiene o establece el identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="d9f92-134">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="d9f92-135">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="d9f92-135">**Repetition**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition)<br/>                    | <span data-ttu-id="d9f92-136">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d9f92-136">Read/write</span></span><br/> | <span data-ttu-id="d9f92-137">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d9f92-137">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d9f92-138">Obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="d9f92-138">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="d9f92-139">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="d9f92-139">**StartBoundary**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary)<br/>              | <span data-ttu-id="d9f92-140">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d9f92-140">Read/write</span></span><br/> | <span data-ttu-id="d9f92-141">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d9f92-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d9f92-142">Obtiene o establece la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="d9f92-142">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="d9f92-143">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="d9f92-143">**StateChange**</span></span>](sessionstatechangetrigger-statechange.md)<br/> | <span data-ttu-id="d9f92-144">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d9f92-144">Read/write</span></span><br/> | <span data-ttu-id="d9f92-145">Obtiene o establece el tipo de cambio de sesión de Terminal Server que desencadenaría un inicio de tarea.</span><span class="sxs-lookup"><span data-stu-id="d9f92-145">Gets or sets the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="d9f92-146">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d9f92-146">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                | <span data-ttu-id="d9f92-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d9f92-147">Read-only</span></span><br/>  | <span data-ttu-id="d9f92-148">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d9f92-148">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d9f92-149">Obtiene el tipo del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="d9f92-149">Gets the type of the trigger.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="d9f92-150">**Deberían**</span><span class="sxs-lookup"><span data-stu-id="d9f92-150">**UserId**</span></span>](sessionstatechangetrigger-userid.md)<br/>           | <span data-ttu-id="d9f92-151">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d9f92-151">Read/write</span></span><br/> | <span data-ttu-id="d9f92-152">Obtiene o establece el usuario para la sesión de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="d9f92-152">Gets or sets the user for the Terminal Server session.</span></span> <span data-ttu-id="d9f92-153">Cuando se detecta un cambio de estado de sesión para este usuario, se inicia una tarea.</span><span class="sxs-lookup"><span data-stu-id="d9f92-153">When a session state change is detected for this user, a task is started.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="d9f92-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9f92-154">Remarks</span></span>

<span data-ttu-id="d9f92-155">Al leer o escribir su propio XML para una tarea, se especifica un desencadenador de cambio de estado de sesión mediante el elemento [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="d9f92-155">When reading or writing your own XML for a task, a session state change trigger is specified using the [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f92-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9f92-156">Requirements</span></span>



| <span data-ttu-id="d9f92-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9f92-157">Requirement</span></span> | <span data-ttu-id="d9f92-158">Value</span><span class="sxs-lookup"><span data-stu-id="d9f92-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f92-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9f92-159">Minimum supported client</span></span><br/> | <span data-ttu-id="d9f92-160">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d9f92-160">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d9f92-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9f92-161">Minimum supported server</span></span><br/> | <span data-ttu-id="d9f92-162">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9f92-162">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d9f92-163">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d9f92-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="d9f92-164"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d9f92-164"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d9f92-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9f92-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9f92-166"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9f92-166"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f92-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9f92-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f92-168">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="d9f92-168">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="d9f92-169">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="d9f92-169">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





