---
title: Elemento EventTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- desencadenador de evento Programador de tareas, elemento
- Elemento EventTrigger Programador de tareas
topic_type:
- apiref
api_name:
- EventTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3cecf46250fface0f716adbf287cda3269b86f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492071"
---
# <a name="eventtrigger-triggergroup-element"></a><span data-ttu-id="da321-105">Elemento EventTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="da321-105">EventTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="da321-106">Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="da321-106">Specifies a trigger that starts a task when a system event occurs.</span></span>

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

<span data-ttu-id="da321-107">El elemento **EventTrigger** está definido por [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="da321-107">The **EventTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="da321-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="da321-108">Parent element</span></span>



| <span data-ttu-id="da321-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="da321-109">Element</span></span>                                                           | <span data-ttu-id="da321-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="da321-110">Derived from</span></span>                                                         | <span data-ttu-id="da321-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="da321-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="da321-112">**Desencadenadores**</span><span class="sxs-lookup"><span data-stu-id="da321-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="da321-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="da321-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="da321-114">Especifica los desencadenadores que inician la tarea.</span><span class="sxs-lookup"><span data-stu-id="da321-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="da321-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="da321-115">Child elements</span></span>



| <span data-ttu-id="da321-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="da321-116">Element</span></span>                                                                                              | <span data-ttu-id="da321-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="da321-117">Type</span></span>                                                                     | <span data-ttu-id="da321-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="da321-118">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da321-119">**Retraso (eventTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="da321-119">**Delay (eventTriggerType)**</span></span>](taskschedulerschema-delay-eventtriggertype-element.md)               | <span data-ttu-id="da321-120">duration</span><span class="sxs-lookup"><span data-stu-id="da321-120">duration</span></span>                                                                 | <span data-ttu-id="da321-121">Especifica la cantidad de tiempo entre el momento en que se produce el evento y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="da321-121">Specifies the amount of time between when the event occurs and when the task is started.</span></span><br/>                                |
| [<span data-ttu-id="da321-122">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="da321-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)             | <span data-ttu-id="da321-123">boolean</span><span class="sxs-lookup"><span data-stu-id="da321-123">boolean</span></span>                                                                  | <span data-ttu-id="da321-124">Especifica que el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="da321-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="da321-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="da321-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)     | <span data-ttu-id="da321-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="da321-126">dateTime</span></span>                                                                 | <span data-ttu-id="da321-127">Especifica la fecha y hora de desactivación del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="da321-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="da321-128">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="da321-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="da321-129">**Repetición (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="da321-129">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)       | [<span data-ttu-id="da321-130">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="da321-130">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="da321-131">Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="da321-131">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="da321-132">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="da321-132">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md) | <span data-ttu-id="da321-133">dateTime</span><span class="sxs-lookup"><span data-stu-id="da321-133">dateTime</span></span>                                                                 | <span data-ttu-id="da321-134">Especifica la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="da321-134">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="da321-135">**Suscripción (eventTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="da321-135">**Subscription (eventTriggerType)**</span></span>](taskschedulerschema-subscription-eventtriggertype-element.md) | <span data-ttu-id="da321-136">string</span><span class="sxs-lookup"><span data-stu-id="da321-136">string</span></span>                                                                   | <span data-ttu-id="da321-137">Especifica la consulta XPath que identifica el evento que activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="da321-137">Specifies the XPath query that identifies the event that fires the trigger.</span></span><br/>                                             |



## <a name="attributes"></a><span data-ttu-id="da321-138">Atributos</span><span class="sxs-lookup"><span data-stu-id="da321-138">Attributes</span></span>



| <span data-ttu-id="da321-139">Nombre</span><span class="sxs-lookup"><span data-stu-id="da321-139">Name</span></span> | <span data-ttu-id="da321-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="da321-140">Type</span></span> | <span data-ttu-id="da321-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="da321-141">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="da321-142">Identificador</span><span class="sxs-lookup"><span data-stu-id="da321-142">Id</span></span>   | <span data-ttu-id="da321-143">id</span><span class="sxs-lookup"><span data-stu-id="da321-143">ID</span></span>   | <span data-ttu-id="da321-144">Identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="da321-144">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="da321-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da321-145">Remarks</span></span>

<span data-ttu-id="da321-146">Se puede crear un máximo de 500 tareas con suscripciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="da321-146">A maximum of 500 tasks with event subscriptions can be created.</span></span> <span data-ttu-id="da321-147">Una suscripción de eventos que consulta diversos eventos se puede usar para desencadenar una tarea que utiliza la misma acción en respuesta a los eventos que se registran.</span><span class="sxs-lookup"><span data-stu-id="da321-147">An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.</span></span>

<span data-ttu-id="da321-148">Para el desarrollo de scripts, el objeto [**EventTrigger**](eventtrigger.md) define un desencadenador de eventos.</span><span class="sxs-lookup"><span data-stu-id="da321-148">For script development, an event trigger is defined by the [**EventTrigger**](eventtrigger.md) object.</span></span>

<span data-ttu-id="da321-149">En el desarrollo de C++, un desencadenador de eventos se define mediante la interfaz [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) .</span><span class="sxs-lookup"><span data-stu-id="da321-149">For C++ development, an event trigger is defined by the [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="da321-150">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="da321-150">Examples</span></span>

<span data-ttu-id="da321-151">Para obtener un ejemplo completo del XML de una tarea que utiliza un desencadenador de eventos, vea [ejemplo de desencadenador de eventos (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="da321-151">For a complete example of the XML for a task that uses an event trigger, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="da321-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da321-152">Requirements</span></span>



| <span data-ttu-id="da321-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="da321-153">Requirement</span></span> | <span data-ttu-id="da321-154">Value</span><span class="sxs-lookup"><span data-stu-id="da321-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="da321-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da321-155">Minimum supported client</span></span><br/> | <span data-ttu-id="da321-156">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="da321-156">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="da321-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da321-157">Minimum supported server</span></span><br/> | <span data-ttu-id="da321-158">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="da321-158">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da321-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="da321-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da321-160">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="da321-160">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

