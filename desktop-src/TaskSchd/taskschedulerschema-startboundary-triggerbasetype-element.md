---
title: Elemento StartBoundary (triggerBaseType)
description: Especifica la fecha y hora en que se activa el desencadenador.
ms.assetid: 95a62ae5-4eba-49df-a25f-0d1181772833
keywords:
- Programador de tareas del elemento StartBoundary
topic_type:
- apiref
api_name:
- StartBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d6adf90de2f3b199f98737996fe732f342787b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150044"
---
# <a name="startboundary-triggerbasetype-element"></a><span data-ttu-id="b2f4d-104">Elemento StartBoundary (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="b2f4d-104">StartBoundary (triggerBaseType) Element</span></span>

<span data-ttu-id="b2f4d-105">Especifica la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="b2f4d-105">Specifies the date and time when the trigger is activated.</span></span>

``` syntax
<xs:element name="StartBoundary"
    type="dateTime"
 />
```

<span data-ttu-id="b2f4d-106">El elemento **StartBoundary** se define mediante el tipo complejo de [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b2f4d-106">The **StartBoundary** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b2f4d-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="b2f4d-107">Parent element</span></span>



| <span data-ttu-id="b2f4d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b2f4d-108">Element</span></span>                                                                                     | <span data-ttu-id="b2f4d-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="b2f4d-109">Derived from</span></span>                                                                               | <span data-ttu-id="b2f4d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2f4d-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2f4d-111">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="b2f4d-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="b2f4d-112">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b2f4d-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="b2f4d-113">Especifica un desencadenador que inicia una tarea cuando se inicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="b2f4d-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="b2f4d-114">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="b2f4d-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="b2f4d-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b2f4d-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="b2f4d-116">Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.</span><span class="sxs-lookup"><span data-stu-id="b2f4d-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="b2f4d-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="b2f4d-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="b2f4d-118">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b2f4d-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="b2f4d-119">Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="b2f4d-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="b2f4d-120">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="b2f4d-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="b2f4d-121">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b2f4d-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="b2f4d-122">Especifica un desencadenador que inicia una tarea cuando el equipo entra en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="b2f4d-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="b2f4d-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="b2f4d-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="b2f4d-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b2f4d-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="b2f4d-125">Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="b2f4d-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="b2f4d-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="b2f4d-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="b2f4d-127">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b2f4d-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="b2f4d-128">Especifica un desencadenador que inicia una tarea cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="b2f4d-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="b2f4d-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="b2f4d-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="b2f4d-130">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b2f4d-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="b2f4d-131">Especifica un desencadenador que inicia una tarea cuando se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="b2f4d-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="b2f4d-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2f4d-132">Remarks</span></span>

<span data-ttu-id="b2f4d-133">El **<StartBoundary>** elemento es un elemento necesario para los desencadenadores Time y Calendar ( [**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) y [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md) ).</span><span class="sxs-lookup"><span data-stu-id="b2f4d-133">The **<StartBoundary>** element is a required element for time and calendar triggers ([**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) and [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="b2f4d-134">Para el desarrollo de scripting, el límite final se especifica mediante la propiedad [**Trigger. StartBoundary**](trigger-startboundary.md) heredada por todos los objetos del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="b2f4d-134">For scripting development, the end boundary is specified using the [**Trigger.StartBoundary**](trigger-startboundary.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="b2f4d-135">En el desarrollo de C++, el límite final se especifica mediante la propiedad [**ITrigger:: StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) heredada por todas las interfaces del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="b2f4d-135">For C++ development, the end boundary is specified using the [**ITrigger::StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) property that is inherited by the all trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="b2f4d-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b2f4d-136">Examples</span></span>

<span data-ttu-id="b2f4d-137">En el código XML siguiente se define un elemento de desencadenador de arranque que define un límite de inicio del 1 de enero de 2005:8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="b2f4d-137">The following XML defines a boot trigger element that defines a start boundary of January 1, 2005: 8:00 AM.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b2f4d-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2f4d-138">Requirements</span></span>



| <span data-ttu-id="b2f4d-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2f4d-139">Requirement</span></span> | <span data-ttu-id="b2f4d-140">Value</span><span class="sxs-lookup"><span data-stu-id="b2f4d-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b2f4d-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2f4d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b2f4d-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b2f4d-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b2f4d-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2f4d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b2f4d-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2f4d-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2f4d-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2f4d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f4d-146">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="b2f4d-146">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b2f4d-147">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="b2f4d-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





