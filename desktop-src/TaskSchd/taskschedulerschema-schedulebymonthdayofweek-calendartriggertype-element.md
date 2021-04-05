---
title: Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)
description: Especifica una programación mensual de día de la semana.
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- Programador de tareas del elemento ScheduleByMonthDayOfWeek
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e92d6ad530466a2238c8239c9e262f85ae361d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803319"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a><span data-ttu-id="b8497-104">Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="b8497-104">ScheduleByMonthDayOfWeek (calendarTriggerType) Element</span></span>

<span data-ttu-id="b8497-105">Especifica una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="b8497-105">Specifies a monthly day-of-week schedule.</span></span> <span data-ttu-id="b8497-106">Por ejemplo, la tarea se inicia en determinados días de la semana, semanas del mes y meses del año.</span><span class="sxs-lookup"><span data-stu-id="b8497-106">For example, the task starts on specific days of the week, weeks of the month, and months of the year.</span></span>

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

<span data-ttu-id="b8497-107">El elemento **ScheduleByMonthDayOfWeek** se define mediante el tipo complejo de [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b8497-107">The **ScheduleByMonthDayOfWeek** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b8497-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="b8497-108">Parent element</span></span>



| <span data-ttu-id="b8497-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="b8497-109">Element</span></span>                                                                             | <span data-ttu-id="b8497-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="b8497-110">Derived from</span></span>                                                                       | <span data-ttu-id="b8497-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8497-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8497-112">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="b8497-112">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="b8497-113">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b8497-113">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="b8497-114">Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.</span><span class="sxs-lookup"><span data-stu-id="b8497-114">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="b8497-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b8497-115">Child elements</span></span>



| <span data-ttu-id="b8497-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="b8497-116">Element</span></span>                                                                                   | <span data-ttu-id="b8497-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8497-117">Type</span></span>                                                                     | <span data-ttu-id="b8497-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8497-118">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="b8497-119">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="b8497-119">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="b8497-120">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="b8497-120">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="b8497-121">Especifica los días de la semana en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="b8497-121">Specifies the days of the week in which the task runs.</span></span><br/>       |
| [<span data-ttu-id="b8497-122">**Partir**</span><span class="sxs-lookup"><span data-stu-id="b8497-122">**Months**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [<span data-ttu-id="b8497-123">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="b8497-123">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)         | <span data-ttu-id="b8497-124">Especifica los meses del año en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="b8497-124">Specifies the months of the year during which the task runs.</span></span><br/> |
| [<span data-ttu-id="b8497-125">**Semanas**</span><span class="sxs-lookup"><span data-stu-id="b8497-125">**Weeks**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | <span data-ttu-id="b8497-126">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="b8497-126">unsignedByte</span></span>                                                             | <span data-ttu-id="b8497-127">Especifica el intervalo entre las semanas de la programación.</span><span class="sxs-lookup"><span data-stu-id="b8497-127">Specifies the interval between the weeks in the schedule.</span></span><br/>    |



## <a name="remarks"></a><span data-ttu-id="b8497-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8497-128">Remarks</span></span>

<span data-ttu-id="b8497-129">La hora del día en que se inicia la tarea se establece mediante el elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b8497-129">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="b8497-130">Para el desarrollo de scripting, se especifica un desencadenador de día de la semana mensual mediante el objeto [**MonthlyDOWTrigger**](monthlydowtrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="b8497-130">For scripting development, a monthly day-of-week trigger is specified using the [**MonthlyDOWTrigger**](monthlydowtrigger.md) object.</span></span>

<span data-ttu-id="b8497-131">En el desarrollo de C++, se especifica un desencadenador de día de la semana mensual mediante la interfaz [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) .</span><span class="sxs-lookup"><span data-stu-id="b8497-131">For C++ development, a monthly day-of-week trigger is specified using the [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) interface.</span></span>

<span data-ttu-id="b8497-132">Los elementos secundarios enumerados anteriormente se definen mediante los tipos de elementos complejos de [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b8497-132">The child elements listed above are defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex element types.</span></span>

## <a name="examples"></a><span data-ttu-id="b8497-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b8497-133">Examples</span></span>

<span data-ttu-id="b8497-134">El siguiente código XML define un desencadenador de calendario mensual de un día de la semana que inicia una tarea (a las 8:00 A.M.) el lunes de la primera semana para cada mes del año.</span><span class="sxs-lookup"><span data-stu-id="b8497-134">The following XML defines a monthly day of week calendar trigger that starts a task ( at 8:00 AM) on Monday of the first week for each month of the year.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonthDayOfWeek>
        <Weeks>
            <Week>1</Week>
        </Weeks>
        <DaysOfWeek>
            <Monday/>
        </DaysOfWeek>
        <Months>
            <January/>
            <February/>
            <March/>
            <April/>
            <May/>
            <June/>
            <July/>
            <August/>
            <September/>
            <October/>
            <November/>
            <December/>
        <Months>
    </ScheduleByMonthDayOfWeek>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="b8497-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8497-135">Requirements</span></span>



| <span data-ttu-id="b8497-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8497-136">Requirement</span></span> | <span data-ttu-id="b8497-137">Value</span><span class="sxs-lookup"><span data-stu-id="b8497-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b8497-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8497-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b8497-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b8497-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b8497-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8497-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b8497-141">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8497-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8497-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8497-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8497-143">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="b8497-143">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b8497-144">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="b8497-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





