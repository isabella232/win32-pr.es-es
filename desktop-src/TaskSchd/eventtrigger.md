---
title: Objeto EventTrigger (Windows. UI. Xaml. h)
description: Objeto de scripting que representa un desencadenador que inicia una tarea cuando se produce un evento del sistema.
ms.assetid: 79cb6591-0919-441f-ad7f-4eb7cf0f9591
keywords:
- desencadenador de evento Programador de tareas, objeto
- Objeto EventTrigger Programador de tareas
- Objeto EventTrigger Programador de tareas, descrito
topic_type:
- apiref
api_name:
- EventTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b80bc8336c4756dfedc041aea40f79fd5f868e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534990"
---
# <a name="eventtrigger-object"></a><span data-ttu-id="6a49f-106">EventTrigger (objeto)</span><span class="sxs-lookup"><span data-stu-id="6a49f-106">EventTrigger object</span></span>

<span data-ttu-id="6a49f-107">Objeto de scripting que representa un desencadenador que inicia una tarea cuando se produce un evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="6a49f-107">Scripting object that represents a trigger that starts a task when a system event occurs.</span></span>

## <a name="members"></a><span data-ttu-id="6a49f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6a49f-108">Members</span></span>

<span data-ttu-id="6a49f-109">El objeto **EventTrigger** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6a49f-109">The **EventTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="6a49f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6a49f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6a49f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6a49f-111">Properties</span></span>

<span data-ttu-id="6a49f-112">El objeto **EventTrigger** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6a49f-112">The **EventTrigger** object has these properties.</span></span>



| <span data-ttu-id="6a49f-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6a49f-113">Property</span></span>                                                            | <span data-ttu-id="6a49f-114">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="6a49f-114">Access type</span></span>           | <span data-ttu-id="6a49f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a49f-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a49f-116">**Delay**</span><span class="sxs-lookup"><span data-stu-id="6a49f-116">**Delay**</span></span>](eventtrigger-delay.md)<br/>                      | <span data-ttu-id="6a49f-117">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6a49f-117">Read/write</span></span><br/> | <span data-ttu-id="6a49f-118">Obtiene o establece un valor que indica la cantidad de tiempo entre el momento en que se produce el evento y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="6a49f-118">Gets or sets a value that indicates the amount of time between when the event occurs and when the task is started.</span></span><br/>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="6a49f-119">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="6a49f-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="6a49f-120">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6a49f-120">Read/write</span></span><br/> | <span data-ttu-id="6a49f-121">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="6a49f-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6a49f-122">Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="6a49f-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="6a49f-123">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="6a49f-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="6a49f-124">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6a49f-124">Read/write</span></span><br/> | <span data-ttu-id="6a49f-125">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="6a49f-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6a49f-126">Obtiene o establece la fecha y hora en que se desactiva el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="6a49f-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="6a49f-127">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="6a49f-127">The trigger cannot start the task after it is deactivated.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="6a49f-128">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="6a49f-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="6a49f-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6a49f-129">Read/write</span></span><br/> | <span data-ttu-id="6a49f-130">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="6a49f-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6a49f-131">Obtiene o establece la cantidad máxima de tiempo que se permite la ejecución de la tarea iniciada por este desencadenador.</span><span class="sxs-lookup"><span data-stu-id="6a49f-131">Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.</span></span><br/>                                                                                                                                                                                                                       |
| [<span data-ttu-id="6a49f-132">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="6a49f-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="6a49f-133">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6a49f-133">Read/write</span></span><br/> | <span data-ttu-id="6a49f-134">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="6a49f-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6a49f-135">Obtiene o establece el identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="6a49f-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="6a49f-136">**Repetición**</span><span class="sxs-lookup"><span data-stu-id="6a49f-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="6a49f-137">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6a49f-137">Read/write</span></span><br/> | <span data-ttu-id="6a49f-138">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="6a49f-138">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6a49f-139">Obtiene o establece la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="6a49f-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>                                                                                                                                                                                                       |
| [<span data-ttu-id="6a49f-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="6a49f-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="6a49f-141">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6a49f-141">Read/write</span></span><br/> | <span data-ttu-id="6a49f-142">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="6a49f-142">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6a49f-143">Obtiene o establece la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="6a49f-143">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="6a49f-144">**Subscription**</span><span class="sxs-lookup"><span data-stu-id="6a49f-144">**Subscription**</span></span>](eventtrigger-subscription.md)<br/>        | <span data-ttu-id="6a49f-145">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6a49f-145">Read/write</span></span><br/> | <span data-ttu-id="6a49f-146">Obtiene o establece la cadena de consulta XPath que identifica el evento que activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="6a49f-146">Gets or sets the XPath query string that identifies the event that fires the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="6a49f-147">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6a49f-147">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="6a49f-148">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a49f-148">Read-only</span></span><br/>  | <span data-ttu-id="6a49f-149">Heredado del objeto [**desencadenador**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="6a49f-149">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6a49f-150">Obtiene el tipo del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="6a49f-150">Gets the type of the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="6a49f-151">**ValueQueries**</span><span class="sxs-lookup"><span data-stu-id="6a49f-151">**ValueQueries**</span></span>](eventtrigger-valuequeries.md)<br/>        | <span data-ttu-id="6a49f-152">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6a49f-152">Read/write</span></span><br/> | <span data-ttu-id="6a49f-153">Obtiene o establece una colección de consultas XPath con nombre.</span><span class="sxs-lookup"><span data-stu-id="6a49f-153">Gets or sets a collection of named XPath queries.</span></span> <span data-ttu-id="6a49f-154">Cada consulta de la colección se aplica al último XML de evento coincidente que se devuelve de la consulta de suscripción especificada en la propiedad de [**suscripción**](eventtrigger-subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="6a49f-154">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](eventtrigger-subscription.md) property.</span></span> <span data-ttu-id="6a49f-155">El nombre de la consulta se puede usar como una variable en el mensaje de una acción [**ShowMessageAction**](showmessageaction.md) .</span><span class="sxs-lookup"><span data-stu-id="6a49f-155">The name of the query can be used as a variable in the message of a [**ShowMessageAction**](showmessageaction.md) action.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a49f-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a49f-156">Remarks</span></span>

<span data-ttu-id="6a49f-157">Se puede crear un máximo de 500 tareas con suscripciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a49f-157">A maximum of 500 tasks with event subscriptions can be created.</span></span> <span data-ttu-id="6a49f-158">Una suscripción de eventos que consulta diversos eventos se puede usar para desencadenar una tarea que utiliza la misma acción en respuesta a los eventos que se registran.</span><span class="sxs-lookup"><span data-stu-id="6a49f-158">An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.</span></span>

<span data-ttu-id="6a49f-159">Al leer o escribir su propio XML para una tarea, se especifica un desencadenador de eventos mediante el elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="6a49f-159">When reading or writing your own XML for a task, an event trigger is specified using the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="6a49f-160">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6a49f-160">Examples</span></span>

<span data-ttu-id="6a49f-161">Para obtener más información y un ejemplo de código para este objeto de scripting, vea [ejemplo de desencadenador de eventos (scripting)](/previous-versions//aa446887(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6a49f-161">For more information and a code example for this scripting object, see [Event Trigger Example (Scripting)](/previous-versions//aa446887(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a49f-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a49f-162">Requirements</span></span>



| <span data-ttu-id="6a49f-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a49f-163">Requirement</span></span> | <span data-ttu-id="6a49f-164">Value</span><span class="sxs-lookup"><span data-stu-id="6a49f-164">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a49f-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a49f-165">Minimum supported client</span></span><br/> | <span data-ttu-id="6a49f-166">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6a49f-166">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6a49f-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a49f-167">Minimum supported server</span></span><br/> | <span data-ttu-id="6a49f-168">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a49f-168">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6a49f-169">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a49f-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a49f-170"><dt>Windows. UI. Xaml. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a49f-170"><dt>Windows.ui.xaml.h</dt></span></span> </dl> |
| <span data-ttu-id="6a49f-171">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6a49f-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="6a49f-172"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6a49f-172"><dt>Taskschd.tlb</dt></span></span> </dl>      |
| <span data-ttu-id="6a49f-173">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6a49f-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a49f-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a49f-174"><dt>Taskschd.dll</dt></span></span> </dl>      |



## <a name="see-also"></a><span data-ttu-id="6a49f-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a49f-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a49f-176">**Activado**</span><span class="sxs-lookup"><span data-stu-id="6a49f-176">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="6a49f-177">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="6a49f-177">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="6a49f-178">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="6a49f-178">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

