---
title: Elemento CalendarTrigger (triggerGroup)
description: Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.
ms.assetid: 9b9218bf-222c-4ece-8b37-5c5d8b765015
keywords:
- desencadenador de calendario Programador de tareas, elemento XML
- Programador de tareas del elemento CalendarTrigger
topic_type:
- apiref
api_name:
- CalendarTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02c061d8821dffa82eca8756ab26acadc6bb9281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686080"
---
# <a name="calendartrigger-triggergroup-element"></a><span data-ttu-id="37ab4-105">Elemento CalendarTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="37ab4-105">CalendarTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="37ab4-106">Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.</span><span class="sxs-lookup"><span data-stu-id="37ab4-106">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span>

``` syntax
<xs:element name="CalendarTrigger"
    type="calendarTriggerType"
 />
```

<span data-ttu-id="37ab4-107">El elemento **CalendarTrigger** se define mediante el tipo complejo de [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="37ab4-107">The **CalendarTrigger** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="37ab4-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="37ab4-108">Parent element</span></span>



| <span data-ttu-id="37ab4-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="37ab4-109">Element</span></span>                                                           | <span data-ttu-id="37ab4-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="37ab4-110">Derived from</span></span>                                                         | <span data-ttu-id="37ab4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="37ab4-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="37ab4-112">**Desencadenadores**</span><span class="sxs-lookup"><span data-stu-id="37ab4-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="37ab4-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="37ab4-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="37ab4-114">Especifica los desencadenadores que inician la tarea.</span><span class="sxs-lookup"><span data-stu-id="37ab4-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="37ab4-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="37ab4-115">Child elements</span></span>



| <span data-ttu-id="37ab4-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="37ab4-116">Element</span></span>                                                                                                                            | <span data-ttu-id="37ab4-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="37ab4-117">Type</span></span>                                                                                                 | <span data-ttu-id="37ab4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="37ab4-118">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37ab4-119">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="37ab4-119">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                                           | <span data-ttu-id="37ab4-120">boolean</span><span class="sxs-lookup"><span data-stu-id="37ab4-120">boolean</span></span>                                                                                              | <span data-ttu-id="37ab4-121">Especifica que el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="37ab4-121">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="37ab4-122">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="37ab4-122">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)                                   | <span data-ttu-id="37ab4-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="37ab4-123">dateTime</span></span>                                                                                             | <span data-ttu-id="37ab4-124">Especifica la fecha y hora de desactivación del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="37ab4-124">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="37ab4-125">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="37ab4-125">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="37ab4-126">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="37ab4-126">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)                     | <span data-ttu-id="37ab4-127">duration</span><span class="sxs-lookup"><span data-stu-id="37ab4-127">duration</span></span>                                                                                             | <span data-ttu-id="37ab4-128">Especifica la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="37ab4-128">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="37ab4-129">**Repetición (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="37ab4-129">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                                     | [<span data-ttu-id="37ab4-130">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="37ab4-130">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md)                             | <span data-ttu-id="37ab4-131">Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="37ab4-131">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="37ab4-132">**ScheduleByDay (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="37ab4-132">**ScheduleByDay (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [<span data-ttu-id="37ab4-133">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="37ab4-133">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)                       | <span data-ttu-id="37ab4-134">Especifica una programación diaria.</span><span class="sxs-lookup"><span data-stu-id="37ab4-134">Specifies a daily schedule.</span></span><br/>                                                                                             |
| [<span data-ttu-id="37ab4-135">**ScheduleByMonth (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="37ab4-135">**ScheduleByMonth (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [<span data-ttu-id="37ab4-136">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="37ab4-136">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)                   | <span data-ttu-id="37ab4-137">Especifica una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="37ab4-137">Specifies a monthly schedule.</span></span><br/>                                                                                           |
| [<span data-ttu-id="37ab4-138">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="37ab4-138">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="37ab4-139">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="37ab4-139">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="37ab4-140">Especifica un desencadenador que inicia un trabajo en una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="37ab4-140">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span><br/>                                                |
| [<span data-ttu-id="37ab4-141">**ScheduleByWeek (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="37ab4-141">**ScheduleByWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [<span data-ttu-id="37ab4-142">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="37ab4-142">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)                     | <span data-ttu-id="37ab4-143">Especifica una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="37ab4-143">Specifies a weekly schedule.</span></span><br/>                                                                                            |
| [<span data-ttu-id="37ab4-144">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="37ab4-144">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)                               | <span data-ttu-id="37ab4-145">dateTime</span><span class="sxs-lookup"><span data-stu-id="37ab4-145">dateTime</span></span>                                                                                             | <span data-ttu-id="37ab4-146">Especifica la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="37ab4-146">Specifies the date and time when the trigger is activated.</span></span> <span data-ttu-id="37ab4-147">Este elemento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="37ab4-147">This element is required.</span></span><br/>                                    |



## <a name="attributes"></a><span data-ttu-id="37ab4-148">Atributos</span><span class="sxs-lookup"><span data-stu-id="37ab4-148">Attributes</span></span>



| <span data-ttu-id="37ab4-149">Nombre</span><span class="sxs-lookup"><span data-stu-id="37ab4-149">Name</span></span> | <span data-ttu-id="37ab4-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="37ab4-150">Type</span></span> | <span data-ttu-id="37ab4-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="37ab4-151">Description</span></span>                               |
|------|------|-------------------------------------------|
| <span data-ttu-id="37ab4-152">Identificador</span><span class="sxs-lookup"><span data-stu-id="37ab4-152">Id</span></span>   | <span data-ttu-id="37ab4-153">id</span><span class="sxs-lookup"><span data-stu-id="37ab4-153">ID</span></span>   | <span data-ttu-id="37ab4-154">Identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="37ab4-154">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="37ab4-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37ab4-155">Remarks</span></span>

<span data-ttu-id="37ab4-156">El elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores de tiempo y calendario ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) y **CalendarTrigger**).</span><span class="sxs-lookup"><span data-stu-id="37ab4-156">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) and **CalendarTrigger**).</span></span>

<span data-ttu-id="37ab4-157">Los elementos secundarios enumerados anteriormente se definen mediante los tipos de elementos complejos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) y [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="37ab4-157">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex element types.</span></span>

<span data-ttu-id="37ab4-158">Para el desarrollo de scripts, los desencadenadores de calendario se especifican mediante uno de los siguientes objetos.</span><span class="sxs-lookup"><span data-stu-id="37ab4-158">For script development, calendar triggers are specified using one of the following objects.</span></span>

-   [<span data-ttu-id="37ab4-159">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="37ab4-159">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="37ab4-160">**WeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="37ab4-160">**WeeklyTrigger**</span></span>](weeklytrigger.md)
-   [<span data-ttu-id="37ab4-161">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="37ab4-161">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="37ab4-162">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="37ab4-162">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)

<span data-ttu-id="37ab4-163">En el desarrollo de C++, los desencadenadores de calendario se especifican mediante una de las interfaces siguientes.</span><span class="sxs-lookup"><span data-stu-id="37ab4-163">For C++ development, calendar triggers are specified using one of the following interfaces.</span></span>

-   [<span data-ttu-id="37ab4-164">**IDailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="37ab4-164">**IDailyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [<span data-ttu-id="37ab4-165">**IWeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="37ab4-165">**IWeeklyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)
-   [<span data-ttu-id="37ab4-166">**IMonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="37ab4-166">**IMonthlyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [<span data-ttu-id="37ab4-167">**IMonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="37ab4-167">**IMonthlyDOWTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

## <a name="examples"></a><span data-ttu-id="37ab4-168">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="37ab4-168">Examples</span></span>

<span data-ttu-id="37ab4-169">Para obtener un ejemplo completo del XML de una tarea que especifica un desencadenador de calendario, vea [ejemplo de desencadenador diario (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="37ab4-169">For a complete example of the XML for a task that specifies a calendar trigger, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37ab4-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37ab4-170">Requirements</span></span>



| <span data-ttu-id="37ab4-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="37ab4-171">Requirement</span></span> | <span data-ttu-id="37ab4-172">Value</span><span class="sxs-lookup"><span data-stu-id="37ab4-172">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="37ab4-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37ab4-173">Minimum supported client</span></span><br/> | <span data-ttu-id="37ab4-174">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="37ab4-174">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="37ab4-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37ab4-175">Minimum supported server</span></span><br/> | <span data-ttu-id="37ab4-176">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="37ab4-176">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37ab4-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="37ab4-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37ab4-178">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="37ab4-178">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="37ab4-179">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="37ab4-179">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





