---
title: Elemento ExecutionTimeLimit (triggerBaseType)
description: Especifica la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.
ms.assetid: f78e7c7b-d069-4920-9435-020f6e081eff
keywords:
- Programador de tareas del elemento ExecutionTimeLimit
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fbe56fb0431ab109b1a19030ae6ba20af55492ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492076"
---
# <a name="executiontimelimit-triggerbasetype-element"></a><span data-ttu-id="1194e-104">Elemento ExecutionTimeLimit (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="1194e-104">ExecutionTimeLimit (triggerBaseType) Element</span></span>

<span data-ttu-id="1194e-105">Especifica la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="1194e-105">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span> <span data-ttu-id="1194e-106">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="1194e-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="1194e-107">Para obtener más información acerca del tipo Duration, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="1194e-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
 />
```

<span data-ttu-id="1194e-108">El elemento **ExecutionTimeLimit** se define mediante el tipo complejo de [**triggerBaseType**](taskschedulerschema-boottriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1194e-108">The **ExecutionTimeLimit** element is defined by the [**triggerBaseType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1194e-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="1194e-109">Parent element</span></span>



| <span data-ttu-id="1194e-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="1194e-110">Element</span></span>                                                                                     | <span data-ttu-id="1194e-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="1194e-111">Derived from</span></span>                                                                               | <span data-ttu-id="1194e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1194e-112">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1194e-113">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="1194e-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="1194e-114">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="1194e-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="1194e-115">Especifica un desencadenador que inicia una tarea cuando se inicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="1194e-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="1194e-116">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="1194e-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="1194e-117">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="1194e-117">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="1194e-118">Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.</span><span class="sxs-lookup"><span data-stu-id="1194e-118">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="1194e-119">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="1194e-119">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="1194e-120">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="1194e-120">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="1194e-121">Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="1194e-121">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="1194e-122">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="1194e-122">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="1194e-123">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="1194e-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="1194e-124">Especifica un desencadenador que inicia una tarea cuando el equipo entra en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="1194e-124">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="1194e-125">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="1194e-125">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="1194e-126">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="1194e-126">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="1194e-127">Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="1194e-127">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="1194e-128">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="1194e-128">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="1194e-129">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="1194e-129">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="1194e-130">Especifica un desencadenador que inicia una tarea cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="1194e-130">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="1194e-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="1194e-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="1194e-132">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="1194e-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="1194e-133">Especifica un desencadenador que inicia una tarea cuando se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="1194e-133">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="1194e-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1194e-134">Remarks</span></span>

<span data-ttu-id="1194e-135">Para el desarrollo de scripting, el límite de tiempo de ejecución se especifica mediante la [**Trigger.Exepropiedad cutionTimeLimit**](trigger-executiontimelimit.md) heredada por todos los objetos de desencadenador.</span><span class="sxs-lookup"><span data-stu-id="1194e-135">For scripting development, the execution time limit is specified using the [**Trigger.ExecutionTimeLimit**](trigger-executiontimelimit.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="1194e-136">En el desarrollo de C++, el límite de tiempo de ejecución se especifica mediante la propiedad [**ITrigger:: ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) heredada por todas las interfaces del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="1194e-136">For C++ development, the execution time limit is specified using the [**ITrigger::ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) property that is inherited by the all trigger interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="1194e-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1194e-137">Requirements</span></span>



| <span data-ttu-id="1194e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="1194e-138">Requirement</span></span> | <span data-ttu-id="1194e-139">Value</span><span class="sxs-lookup"><span data-stu-id="1194e-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1194e-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1194e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1194e-141">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1194e-141">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1194e-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1194e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1194e-143">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1194e-143">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1194e-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="1194e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1194e-145">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="1194e-145">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="1194e-146">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="1194e-146">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





