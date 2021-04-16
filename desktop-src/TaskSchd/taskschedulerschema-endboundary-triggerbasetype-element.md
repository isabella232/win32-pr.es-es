---
title: Elemento EndBoundary (triggerBaseType)
description: Especifica la fecha y hora de desactivación del desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.
ms.assetid: 84731c0b-3fb8-44dd-be1a-67547add1f9e
keywords:
- Programador de tareas del elemento EndBoundary
topic_type:
- apiref
api_name:
- EndBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d687655498301595c1ab888fcc179ec0694f0aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685885"
---
# <a name="endboundary-triggerbasetype-element"></a><span data-ttu-id="353a3-105">Elemento EndBoundary (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="353a3-105">EndBoundary (triggerBaseType) Element</span></span>

<span data-ttu-id="353a3-106">Especifica la fecha y hora de desactivación del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="353a3-106">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="353a3-107">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="353a3-107">The trigger cannot start the task after it is deactivated.</span></span>

``` syntax
<xs:element name="EndBoundary"
    type="dateTime"
 />
```

<span data-ttu-id="353a3-108">El elemento **EndBoundary** se define mediante el tipo complejo de [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="353a3-108">The **EndBoundary** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="353a3-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="353a3-109">Parent element</span></span>



| <span data-ttu-id="353a3-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="353a3-110">Element</span></span>                                                                                     | <span data-ttu-id="353a3-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="353a3-111">Derived from</span></span>                                                                               | <span data-ttu-id="353a3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="353a3-112">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="353a3-113">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="353a3-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="353a3-114">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="353a3-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="353a3-115">Especifica un desencadenador que inicia una tarea cuando se inicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="353a3-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="353a3-116">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="353a3-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="353a3-117">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="353a3-117">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="353a3-118">Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.</span><span class="sxs-lookup"><span data-stu-id="353a3-118">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="353a3-119">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="353a3-119">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="353a3-120">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="353a3-120">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="353a3-121">Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="353a3-121">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="353a3-122">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="353a3-122">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="353a3-123">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="353a3-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="353a3-124">Especifica un desencadenador que inicia una tarea cuando el equipo entra en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="353a3-124">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="353a3-125">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="353a3-125">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="353a3-126">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="353a3-126">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="353a3-127">Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="353a3-127">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="353a3-128">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="353a3-128">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="353a3-129">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="353a3-129">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="353a3-130">Especifica un desencadenador que inicia una tarea cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="353a3-130">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="353a3-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="353a3-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="353a3-132">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="353a3-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="353a3-133">Especifica un desencadenador que inicia una tarea cuando se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="353a3-133">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="353a3-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="353a3-134">Remarks</span></span>

<span data-ttu-id="353a3-135">Para el desarrollo de scripting, el límite final se especifica mediante la propiedad [**Trigger. EndBoundary**](trigger-endboundary.md) heredada por todos los objetos del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="353a3-135">For scripting development, the end boundary is specified using the [**Trigger.EndBoundary**](trigger-endboundary.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="353a3-136">En el desarrollo de C++, el límite final se especifica mediante la propiedad [**ITrigger:: EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) heredada por todas las interfaces del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="353a3-136">For C++ development, the end boundary is specified using the [**ITrigger::EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) property that is inherited by the all trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="353a3-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="353a3-137">Examples</span></span>

<span data-ttu-id="353a3-138">En el código XML siguiente se define un elemento de desencadenador de arranque que define un límite final del 1 de enero de 2007:8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="353a3-138">The following XML defines a boot trigger element that defines an end boundary of January 1, 2007: 8:00 AM.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="353a3-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="353a3-139">Requirements</span></span>



| <span data-ttu-id="353a3-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="353a3-140">Requirement</span></span> | <span data-ttu-id="353a3-141">Value</span><span class="sxs-lookup"><span data-stu-id="353a3-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="353a3-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="353a3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="353a3-143">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="353a3-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="353a3-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="353a3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="353a3-145">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="353a3-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="353a3-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="353a3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="353a3-147">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="353a3-147">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="353a3-148">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="353a3-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





