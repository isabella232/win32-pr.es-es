---
title: Elemento Enabled (triggerBaseType)
description: Especifica que el desencadenador está habilitado.
ms.assetid: 14c98f40-0ec5-4dc1-978e-b02c08ee2384
keywords:
- Programador de tareas de elementos habilitados
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42b495ba1af5f3b9b99034b0d6ca9d02040460c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079765"
---
# <a name="enabled-triggerbasetype-element"></a><span data-ttu-id="87432-104">Elemento Enabled (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="87432-104">Enabled (triggerBaseType) Element</span></span>

<span data-ttu-id="87432-105">Especifica que el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="87432-105">Specifies that the trigger is enabled.</span></span>

``` syntax
<xs:element name="Enabled"
    type="boolean"
 />
```

<span data-ttu-id="87432-106">El elemento **Enabled** se define mediante el tipo complejo de [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="87432-106">The **Enabled** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="87432-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="87432-107">Parent element</span></span>



| <span data-ttu-id="87432-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="87432-108">Element</span></span>                                                                                     | <span data-ttu-id="87432-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="87432-109">Derived from</span></span>                                                                               | <span data-ttu-id="87432-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="87432-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87432-111">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="87432-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="87432-112">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="87432-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="87432-113">Especifica un desencadenador que inicia una tarea cuando se inicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="87432-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="87432-114">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="87432-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="87432-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="87432-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="87432-116">Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.</span><span class="sxs-lookup"><span data-stu-id="87432-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="87432-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="87432-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="87432-118">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="87432-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="87432-119">Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="87432-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="87432-120">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="87432-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="87432-121">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="87432-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="87432-122">Especifica un desencadenador que inicia una tarea cuando el equipo entra en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="87432-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="87432-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="87432-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="87432-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="87432-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="87432-125">Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="87432-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="87432-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="87432-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="87432-127">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="87432-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="87432-128">Especifica un desencadenador que inicia una tarea cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="87432-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="87432-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="87432-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="87432-130">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="87432-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="87432-131">Especifica un desencadenador que inicia una tarea cuando se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="87432-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="87432-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87432-132">Remarks</span></span>

<span data-ttu-id="87432-133">Para el desarrollo de scripting, se tiene acceso a esta información a través de la propiedad [**Trigger. Enabled**](trigger-enabled.md) heredada por todos los objetos Trigger.</span><span class="sxs-lookup"><span data-stu-id="87432-133">For scripting development, this information is accessed through the [**Trigger.Enabled**](trigger-enabled.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="87432-134">En el desarrollo de C++, se obtiene acceso a esta información a través de la propiedad [**ITrigger:: Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) , heredada por todas las interfaces del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="87432-134">For C++ development, this information is accessed through the [**ITrigger::Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) property that is inherited by the all trigger interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="87432-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87432-135">Requirements</span></span>



| <span data-ttu-id="87432-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="87432-136">Requirement</span></span> | <span data-ttu-id="87432-137">Value</span><span class="sxs-lookup"><span data-stu-id="87432-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="87432-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87432-138">Minimum supported client</span></span><br/> | <span data-ttu-id="87432-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="87432-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="87432-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87432-140">Minimum supported server</span></span><br/> | <span data-ttu-id="87432-141">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="87432-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87432-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="87432-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87432-143">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="87432-143">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="87432-144">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="87432-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





