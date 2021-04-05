---
title: Objeto LogonTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea cuando un usuario inicia sesión.
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- Programador de tareas de desencadenador de inicio de sesión, objeto
- Objeto LogonTrigger Programador de tareas
- Programador de tareas de objeto LogonTrigger, descrito
topic_type:
- apiref
api_name:
- LogonTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9c4b2031b39a6dfd483b039023ad9114271b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996690"
---
# <a name="logontrigger-object"></a><span data-ttu-id="c84f0-106">Objeto LogonTrigger</span><span class="sxs-lookup"><span data-stu-id="c84f0-106">LogonTrigger object</span></span>

<span data-ttu-id="c84f0-107">Objeto de scripting que representa un desencadenador que inicia una tarea cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="c84f0-107">Scripting object that represents a trigger that starts a task when a user logs on.</span></span> <span data-ttu-id="c84f0-108">Cuando se inicia el servicio Programador de tareas, se enumeran todos los usuarios que han iniciado sesión y se ejecutan las tareas registradas con desencadenadores Logon que coinciden con el usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="c84f0-108">When the Task Scheduler service starts, all logged-on users are enumerated and any tasks registered with logon triggers that match the logged on user are run.</span></span>

## <a name="members"></a><span data-ttu-id="c84f0-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c84f0-109">Members</span></span>

<span data-ttu-id="c84f0-110">El objeto **LogonTrigger** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c84f0-110">The **LogonTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="c84f0-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c84f0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c84f0-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c84f0-112">Properties</span></span>

<span data-ttu-id="c84f0-113">El objeto **LogonTrigger** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c84f0-113">The **LogonTrigger** object has these properties.</span></span>



| <span data-ttu-id="c84f0-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c84f0-114">Property</span></span>                                                            | <span data-ttu-id="c84f0-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="c84f0-115">Access type</span></span>           | <span data-ttu-id="c84f0-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c84f0-116">Description</span></span>                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c84f0-117">**Delay**</span><span class="sxs-lookup"><span data-stu-id="c84f0-117">**Delay**</span></span>](logontrigger-delay.md)<br/>                      | <span data-ttu-id="c84f0-118">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c84f0-118">Read/write</span></span><br/> | <span data-ttu-id="c84f0-119">Obtiene o establece un valor que indica la cantidad de tiempo entre el momento en el que el usuario inicia sesión y el momento en que se inicia el trabajo.</span><span class="sxs-lookup"><span data-stu-id="c84f0-119">Gets or sets a value that indicates the amount of time between when the user logs on and when the job is started.</span></span><br/>                                                                              |
| [<span data-ttu-id="c84f0-120">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="c84f0-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="c84f0-121">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c84f0-121">Read/write</span></span><br/> | <span data-ttu-id="c84f0-122">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c84f0-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="c84f0-123">Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c84f0-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="c84f0-124">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="c84f0-124">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="c84f0-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c84f0-125">Read/write</span></span><br/> | <span data-ttu-id="c84f0-126">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c84f0-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="c84f0-127">Obtiene o establece la fecha y hora en que se desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="c84f0-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="c84f0-128">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="c84f0-128">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="c84f0-129">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="c84f0-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="c84f0-130">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c84f0-130">Read/write</span></span><br/> | <span data-ttu-id="c84f0-131">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c84f0-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="c84f0-132">Obtiene o establece la cantidad máxima de tiempo que puede ejecutarse la tarea iniciada por el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="c84f0-132">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                                         |
| [<span data-ttu-id="c84f0-133">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="c84f0-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="c84f0-134">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c84f0-134">Read/write</span></span><br/> | <span data-ttu-id="c84f0-135">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c84f0-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="c84f0-136">Obtiene o establece el identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="c84f0-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="c84f0-137">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="c84f0-137">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="c84f0-138">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c84f0-138">Read/write</span></span><br/> | <span data-ttu-id="c84f0-139">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c84f0-139">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="c84f0-140">Obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="c84f0-140">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="c84f0-141">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="c84f0-141">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="c84f0-142">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c84f0-142">Read/write</span></span><br/> | <span data-ttu-id="c84f0-143">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c84f0-143">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="c84f0-144">Obtiene o establece la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="c84f0-144">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="c84f0-145">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c84f0-145">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="c84f0-146">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c84f0-146">Read-only</span></span><br/>  | <span data-ttu-id="c84f0-147">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c84f0-147">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="c84f0-148">Obtiene el tipo del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="c84f0-148">Gets the type of the trigger.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="c84f0-149">**Deberían**</span><span class="sxs-lookup"><span data-stu-id="c84f0-149">**UserId**</span></span>](logontrigger-userid.md)<br/>                    | <span data-ttu-id="c84f0-150">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c84f0-150">Read/write</span></span><br/> | <span data-ttu-id="c84f0-151">Obtiene o establece el identificador del usuario.</span><span class="sxs-lookup"><span data-stu-id="c84f0-151">Gets or sets the identifier of the user.</span></span><br/>                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="c84f0-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c84f0-152">Remarks</span></span>

<span data-ttu-id="c84f0-153">Si desea que una tarea se desencadene cuando un miembro de un grupo inicia sesión en el equipo en lugar de cuando un usuario específico inicia sesión, no asigne un valor a la propiedad [**LogonTrigger. userid**](logontrigger-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="c84f0-153">If you want a task to be triggered when any member of a group logs on to the computer rather than when a specific user logs on, then do not assign a value to the [**LogonTrigger.UserId**](logontrigger-userid.md) property.</span></span> <span data-ttu-id="c84f0-154">En su lugar, cree un desencadenador Logon con una propiedad **LogonTrigger. userid** vacía y asigne un valor a la entidad de seguridad para la tarea mediante la propiedad [**principal. GROUPID**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="c84f0-154">Instead, create a logon trigger with an empty **LogonTrigger.UserId** property and assign a value to the principal for the task using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="c84f0-155">Al leer o escribir XML para una tarea, se especifica un desencadenador Logon mediante el elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) del esquema programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="c84f0-155">When reading or writing XML for a task, a logon trigger is specified using the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="c84f0-156">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c84f0-156">Examples</span></span>

<span data-ttu-id="c84f0-157">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de inicio de sesión (scripting)](logon-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="c84f0-157">For more information and example code for this scripting object, see [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c84f0-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c84f0-158">Requirements</span></span>



| <span data-ttu-id="c84f0-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="c84f0-159">Requirement</span></span> | <span data-ttu-id="c84f0-160">Value</span><span class="sxs-lookup"><span data-stu-id="c84f0-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c84f0-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c84f0-161">Minimum supported client</span></span><br/> | <span data-ttu-id="c84f0-162">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c84f0-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c84f0-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c84f0-163">Minimum supported server</span></span><br/> | <span data-ttu-id="c84f0-164">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c84f0-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c84f0-165">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c84f0-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="c84f0-166"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c84f0-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c84f0-167">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c84f0-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c84f0-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c84f0-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c84f0-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="c84f0-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c84f0-170">**Activado**</span><span class="sxs-lookup"><span data-stu-id="c84f0-170">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





