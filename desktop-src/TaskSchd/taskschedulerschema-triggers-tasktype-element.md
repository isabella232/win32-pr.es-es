---
title: Elemento triggers (taskType)
description: Especifica los desencadenadores que inician la tarea.
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- Desencadenadores (elemento) Programador de tareas
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06994c395fbfbc5b0c6244c9d17930bc4afac885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803967"
---
# <a name="triggers-tasktype-element"></a><span data-ttu-id="85c22-104">Elemento triggers (taskType)</span><span class="sxs-lookup"><span data-stu-id="85c22-104">Triggers (taskType) Element</span></span>

<span data-ttu-id="85c22-105">Especifica los desencadenadores que inician la tarea.</span><span class="sxs-lookup"><span data-stu-id="85c22-105">Specifies the triggers that start the task.</span></span>

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

<span data-ttu-id="85c22-106">El elemento **triggers** se define mediante el tipo complejo [**triggersType**](taskschedulerschema-triggerstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="85c22-106">The **Triggers** element is defined by the [**triggersType**](taskschedulerschema-triggerstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="85c22-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="85c22-107">Parent element</span></span>



| <span data-ttu-id="85c22-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="85c22-108">Element</span></span>                                          | <span data-ttu-id="85c22-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="85c22-109">Derived from</span></span>                                                 | <span data-ttu-id="85c22-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="85c22-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="85c22-111">**Task**</span><span class="sxs-lookup"><span data-stu-id="85c22-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="85c22-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="85c22-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="85c22-113">Define la tarea que realiza el servicio Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="85c22-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="85c22-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="85c22-114">Child elements</span></span>



| <span data-ttu-id="85c22-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="85c22-115">Element</span></span>                                                                                     | <span data-ttu-id="85c22-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="85c22-116">Type</span></span>                                                                                       | <span data-ttu-id="85c22-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="85c22-117">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85c22-118">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="85c22-118">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="85c22-119">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="85c22-119">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="85c22-120">Especifica un desencadenador que inicia una tarea cuando se inicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="85c22-120">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="85c22-121">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="85c22-121">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="85c22-122">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="85c22-122">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="85c22-123">Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.</span><span class="sxs-lookup"><span data-stu-id="85c22-123">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="85c22-124">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="85c22-124">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="85c22-125">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="85c22-125">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="85c22-126">Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="85c22-126">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="85c22-127">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="85c22-127">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="85c22-128">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="85c22-128">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="85c22-129">Especifica un desencadenador que inicia una tarea cuando el equipo entra en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="85c22-129">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="85c22-130">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="85c22-130">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="85c22-131">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="85c22-131">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="85c22-132">Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="85c22-132">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="85c22-133">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="85c22-133">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="85c22-134">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="85c22-134">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="85c22-135">Especifica un desencadenador que inicia una tarea cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="85c22-135">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="85c22-136">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="85c22-136">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="85c22-137">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="85c22-137">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="85c22-138">Especifica un desencadenador que inicia una tarea cuando se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="85c22-138">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="85c22-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85c22-139">Remarks</span></span>

<span data-ttu-id="85c22-140">Los elementos secundarios enumerados anteriormente se pueden agregar en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="85c22-140">The child elements listed above can be added in any order.</span></span>

<span data-ttu-id="85c22-141">En el desarrollo de C++, los desencadenadores de una tarea se especifican mediante la [**propiedad triggers de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).</span><span class="sxs-lookup"><span data-stu-id="85c22-141">For C++ development, the triggers of a task are specified using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).</span></span>

<span data-ttu-id="85c22-142">Para el desarrollo de scripts, los desencadenadores de una tarea se especifican mediante la propiedad [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="85c22-142">For scripting development, the triggers of a task are specified using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="85c22-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="85c22-143">Examples</span></span>

<span data-ttu-id="85c22-144">Para obtener un ejemplo completo del XML de una tarea que especifica un desencadenador, vea [ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="85c22-144">For a complete example of the XML for a task that specifies a trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85c22-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85c22-145">Requirements</span></span>



| <span data-ttu-id="85c22-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="85c22-146">Requirement</span></span> | <span data-ttu-id="85c22-147">Value</span><span class="sxs-lookup"><span data-stu-id="85c22-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="85c22-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85c22-148">Minimum supported client</span></span><br/> | <span data-ttu-id="85c22-149">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="85c22-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="85c22-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85c22-150">Minimum supported server</span></span><br/> | <span data-ttu-id="85c22-151">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="85c22-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85c22-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="85c22-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85c22-153">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="85c22-153">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="85c22-154">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="85c22-154">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





