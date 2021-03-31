---
title: Grupo triggerGroup
description: Define el grupo de desencadenadores.
ms.assetid: e07e6999-d982-405b-adfd-2976707b999f
keywords:
- Programador de tareas triggerGroup
topic_type:
- apiref
api_name:
- triggerGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce0203cd9515808891f93223dd7b3ebaf2642103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151173"
---
# <a name="triggergroup-group"></a><span data-ttu-id="d7eeb-104">Grupo triggerGroup</span><span class="sxs-lookup"><span data-stu-id="d7eeb-104">triggerGroup Group</span></span>

<span data-ttu-id="d7eeb-105">Define el grupo de desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="d7eeb-105">Defines the trigger group.</span></span>

``` syntax
<xs:group name="triggerGroup">
    <xs:choice>
        <xs:element name="BootTrigger"
            type="bootTriggerType"
            minOccurs="0"
         />
        <xs:element name="RegistrationTrigger"
            type="registrationTriggerType"
            minOccurs="0"
         />
        <xs:element name="IdleTrigger"
            type="idleTriggerType"
            minOccurs="0"
         />
        <xs:element name="TimeTrigger"
            type="timeTriggerType"
            minOccurs="0"
         />
        <xs:element name="EventTrigger"
            type="eventTriggerType"
            minOccurs="0"
         />
        <xs:element name="LogonTrigger"
            type="logonTriggerType"
            minOccurs="0"
         />
        <xs:element name="SessionStateChangeTrigger"
            type="sessionStateChangeTriggerType"
            minOccurs="0"
         />
        <xs:element name="CalendarTrigger"
            type="calendarTriggerType"
            minOccurs="0"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="d7eeb-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d7eeb-106">Child elements</span></span>



| <span data-ttu-id="d7eeb-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="d7eeb-107">Element</span></span>                                                                                                 | <span data-ttu-id="d7eeb-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7eeb-108">Type</span></span>                                                                                                   | <span data-ttu-id="d7eeb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7eeb-109">Description</span></span>                                                                                                       |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7eeb-110">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-110">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                             | [<span data-ttu-id="d7eeb-111">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-111">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                             | <span data-ttu-id="d7eeb-112">Desencadenador que inicia una tarea cuando se inicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="d7eeb-112">A trigger that starts a task when the system is booted.</span></span><br/>                                                |
| [<span data-ttu-id="d7eeb-113">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)                     | [<span data-ttu-id="d7eeb-114">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)                     | <span data-ttu-id="d7eeb-115">Desencadenador que inicia una tarea en función de una programación diaria, semanal, mensual o mensual (DOW).</span><span class="sxs-lookup"><span data-stu-id="d7eeb-115">A trigger that starts a task based on a daily, weekly, monthly, or monthly day-of-week (DOW) schedule.</span></span><br/> |
| [<span data-ttu-id="d7eeb-116">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-116">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)                           | [<span data-ttu-id="d7eeb-117">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-117">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)                           | <span data-ttu-id="d7eeb-118">Desencadenador que inicia una tarea cuando se produce un evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="d7eeb-118">A trigger that starts a task when a system event occurs.</span></span><br/>                                               |
| [<span data-ttu-id="d7eeb-119">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-119">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                             | [<span data-ttu-id="d7eeb-120">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-120">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                             | <span data-ttu-id="d7eeb-121">Desencadenador que inicia una tarea cuando el equipo entra en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="d7eeb-121">A trigger that starts a task when the computer goes into an idle state.</span></span><br/>                                |
| [<span data-ttu-id="d7eeb-122">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-122">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)                           | [<span data-ttu-id="d7eeb-123">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-123">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)                           | <span data-ttu-id="d7eeb-124">Desencadenador que inicia una tarea cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="d7eeb-124">A trigger that starts a task when a user logs on.</span></span><br/>                                                      |
| [<span data-ttu-id="d7eeb-125">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-125">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md)             | [<span data-ttu-id="d7eeb-126">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-126">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md)             | <span data-ttu-id="d7eeb-127">Desencadenador que inicia una tarea cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="d7eeb-127">A trigger that starts a task when the task is registered.</span></span><br/>                                              |
| [<span data-ttu-id="d7eeb-128">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-128">**SessionStateChangeTrigger**</span></span>](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) | [<span data-ttu-id="d7eeb-129">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-129">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="d7eeb-130">Desencadenador que inicia una tarea cuando cambia el estado de una sesión de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="d7eeb-130">A trigger that starts a task when a Terminal Server session changes state.</span></span><br/>                             |
| [<span data-ttu-id="d7eeb-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                             | [<span data-ttu-id="d7eeb-132">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d7eeb-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                             | <span data-ttu-id="d7eeb-133">Desencadenador que inicia una tarea cuando se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="d7eeb-133">A trigger that starts a task when the trigger is activated.</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="d7eeb-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7eeb-134">Remarks</span></span>

<span data-ttu-id="d7eeb-135">Al leer o escribir XML, los elementos definidos por este grupo son los elementos secundarios del elemento [**triggers**](taskschedulerschema-triggers-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d7eeb-135">When reading or writing XML, the elements that are defined by this group are the child elements of the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7eeb-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7eeb-136">Requirements</span></span>



| <span data-ttu-id="d7eeb-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7eeb-137">Requirement</span></span> | <span data-ttu-id="d7eeb-138">Value</span><span class="sxs-lookup"><span data-stu-id="d7eeb-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d7eeb-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7eeb-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d7eeb-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d7eeb-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d7eeb-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7eeb-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d7eeb-142">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7eeb-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7eeb-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7eeb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7eeb-144">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="d7eeb-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





