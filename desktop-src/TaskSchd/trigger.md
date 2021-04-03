---
title: Desencadenador (objeto)
description: Objeto de scripting que proporciona las propiedades comunes que heredan todos los objetos de desencadenador.
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- desencadenadores Programador de tareas, objeto desencadenador
- Programador de tareas de objeto desencadenador
- Programador de tareas de objeto desencadenador, descrito
topic_type:
- apiref
api_name:
- Trigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4a7edc6eff0bb04c81ba3bff3bb86ec0455b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905116"
---
# <a name="trigger-object"></a><span data-ttu-id="01e53-106">Desencadenador (objeto)</span><span class="sxs-lookup"><span data-stu-id="01e53-106">Trigger object</span></span>

<span data-ttu-id="01e53-107">Objeto de scripting que proporciona las propiedades comunes que heredan todos los objetos de desencadenador.</span><span class="sxs-lookup"><span data-stu-id="01e53-107">Scripting object that provides the common properties that are inherited by all trigger objects.</span></span>

## <a name="members"></a><span data-ttu-id="01e53-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="01e53-108">Members</span></span>

<span data-ttu-id="01e53-109">El objeto **desencadenador** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="01e53-109">The **Trigger** object has these types of members:</span></span>

-   [<span data-ttu-id="01e53-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01e53-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01e53-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01e53-111">Properties</span></span>

<span data-ttu-id="01e53-112">El objeto **desencadenador** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="01e53-112">The **Trigger** object has these properties.</span></span>



| <span data-ttu-id="01e53-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01e53-113">Property</span></span>                                                            | <span data-ttu-id="01e53-114">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="01e53-114">Access type</span></span>           | <span data-ttu-id="01e53-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="01e53-115">Description</span></span>                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01e53-116">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="01e53-116">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="01e53-117">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="01e53-117">Read/write</span></span><br/> | <span data-ttu-id="01e53-118">Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="01e53-118">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="01e53-119">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="01e53-119">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="01e53-120">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="01e53-120">Read/write</span></span><br/> | <span data-ttu-id="01e53-121">Obtiene o establece la fecha y hora en que se desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="01e53-121">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="01e53-122">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="01e53-122">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="01e53-123">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="01e53-123">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="01e53-124">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="01e53-124">Read/write</span></span><br/> | <span data-ttu-id="01e53-125">Obtiene o establece la cantidad máxima de tiempo que puede ejecutarse la tarea iniciada por el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="01e53-125">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                                         |
| [<span data-ttu-id="01e53-126">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="01e53-126">**Id**</span></span>](trigger-id.md)<br/>                                 | <span data-ttu-id="01e53-127">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="01e53-127">Read/write</span></span><br/> | <span data-ttu-id="01e53-128">Obtiene o establece el identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="01e53-128">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="01e53-129">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="01e53-129">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="01e53-130">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="01e53-130">Read/write</span></span><br/> | <span data-ttu-id="01e53-131">Obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="01e53-131">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="01e53-132">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="01e53-132">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="01e53-133">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="01e53-133">Read/write</span></span><br/> | <span data-ttu-id="01e53-134">Obtiene o establece la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="01e53-134">Gets or sets the date and time when the trigger is activated.</span></span> <span data-ttu-id="01e53-135">El desencadenador puede iniciar la tarea después de activar el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="01e53-135">The trigger can start the task after the trigger is activated.</span></span><br/>             |
| [<span data-ttu-id="01e53-136">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="01e53-136">**Type**</span></span>](trigger-type.md)<br/>                             |                       | <span data-ttu-id="01e53-137">Obtiene el tipo del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="01e53-137">Gets the type of the trigger.</span></span><br/>                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="01e53-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01e53-138">Remarks</span></span>

<span data-ttu-id="01e53-139">En el Programador de tareas se proporcionan los siguientes objetos individuales para los distintos desencadenadores que puede usar una tarea:</span><span class="sxs-lookup"><span data-stu-id="01e53-139">The Task Scheduler provides the following individual objects for the different triggers that a task can use:</span></span>

-   [<span data-ttu-id="01e53-140">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="01e53-140">**BootTrigger**</span></span>](boottrigger.md)
-   [<span data-ttu-id="01e53-141">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="01e53-141">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="01e53-142">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="01e53-142">**EventTrigger**</span></span>](eventtrigger.md)
-   [<span data-ttu-id="01e53-143">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="01e53-143">**IdleTrigger**</span></span>](idletrigger.md)
-   [<span data-ttu-id="01e53-144">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="01e53-144">**LogonTrigger**</span></span>](logontrigger.md)
-   [<span data-ttu-id="01e53-145">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="01e53-145">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
-   [<span data-ttu-id="01e53-146">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="01e53-146">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="01e53-147">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="01e53-147">**RegistrationTrigger**</span></span>](registrationtrigger.md)
-   [<span data-ttu-id="01e53-148">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="01e53-148">**TimeTrigger**</span></span>](timetrigger.md)
-   [<span data-ttu-id="01e53-149">**WeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="01e53-149">**WeeklyTrigger**</span></span>](weeklytrigger.md)
-   [<span data-ttu-id="01e53-150">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="01e53-150">**SessionStateChangeTrigger**</span></span>](sessionstatechangetrigger.md)

<span data-ttu-id="01e53-151">Al leer o escribir XML, los desencadenadores de una tarea se especifican en el elemento [**triggers**](taskschedulerschema-triggers-tasktype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="01e53-151">When reading or writing XML, the triggers of a task are specified in the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="01e53-152">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="01e53-152">Examples</span></span>

<span data-ttu-id="01e53-153">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="01e53-153">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01e53-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01e53-154">Requirements</span></span>



| <span data-ttu-id="01e53-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="01e53-155">Requirement</span></span> | <span data-ttu-id="01e53-156">Value</span><span class="sxs-lookup"><span data-stu-id="01e53-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01e53-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01e53-157">Minimum supported client</span></span><br/> | <span data-ttu-id="01e53-158">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="01e53-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="01e53-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01e53-159">Minimum supported server</span></span><br/> | <span data-ttu-id="01e53-160">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="01e53-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="01e53-161">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="01e53-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="01e53-162"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="01e53-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="01e53-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="01e53-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01e53-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01e53-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01e53-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="01e53-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01e53-166">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="01e53-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> </dl>

 

 





