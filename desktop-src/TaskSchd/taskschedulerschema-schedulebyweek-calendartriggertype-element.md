---
title: Elemento ScheduleByWeek (calendarTriggerType)
description: Especifica una programación semanal.
ms.assetid: d2c33e76-0564-4b3c-ab86-e7bca667fa4f
keywords:
- Programador de tareas de desencadenador semanal, elemento XML
- Programador de tareas del elemento ScheduleByWeek
topic_type:
- apiref
api_name:
- ScheduleByWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d5ab62a0c39c4c1d0102edcdb96d310e9315820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422575"
---
# <a name="schedulebyweek-calendartriggertype-element"></a><span data-ttu-id="96e71-105">Elemento ScheduleByWeek (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="96e71-105">ScheduleByWeek (calendarTriggerType) Element</span></span>

<span data-ttu-id="96e71-106">Especifica una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="96e71-106">Specifies a weekly schedule.</span></span> <span data-ttu-id="96e71-107">Por ejemplo, la tarea comienza a las 8:00 A.M. en un día concreto de la semana cada semana o en un día concreto de la semana, cada dos semanas.</span><span class="sxs-lookup"><span data-stu-id="96e71-107">For example, the task starts at 8:00 AM on a specific day of the week every week or on a specific day of the week every other week.</span></span>

``` syntax
<xs:element name="ScheduleByWeek"
    type="weeklyScheduleType"
 />
```

<span data-ttu-id="96e71-108">El elemento **ScheduleByWeek** se define mediante el tipo complejo de [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="96e71-108">The **ScheduleByWeek** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="96e71-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="96e71-109">Parent element</span></span>



| <span data-ttu-id="96e71-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="96e71-110">Element</span></span>                                                                             | <span data-ttu-id="96e71-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="96e71-111">Derived from</span></span>                                                                       | <span data-ttu-id="96e71-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="96e71-112">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96e71-113">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="96e71-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="96e71-114">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="96e71-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="96e71-115">Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.</span><span class="sxs-lookup"><span data-stu-id="96e71-115">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="96e71-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="96e71-116">Child elements</span></span>



| <span data-ttu-id="96e71-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="96e71-117">Element</span></span>                                                                               | <span data-ttu-id="96e71-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="96e71-118">Type</span></span>                                                                     | <span data-ttu-id="96e71-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="96e71-119">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="96e71-120">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="96e71-120">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [<span data-ttu-id="96e71-121">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="96e71-121">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="96e71-122">Especifica los días de la semana en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="96e71-122">Specifies the days of the week in which the task runs.</span></span><br/>    |
| [<span data-ttu-id="96e71-123">**WeeksInterval**</span><span class="sxs-lookup"><span data-stu-id="96e71-123">**WeeksInterval**</span></span>](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) | <span data-ttu-id="96e71-124">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="96e71-124">unsignedByte</span></span>                                                             | <span data-ttu-id="96e71-125">Especifica el intervalo entre las semanas de la programación.</span><span class="sxs-lookup"><span data-stu-id="96e71-125">Specifies the interval between the weeks in the schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="96e71-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96e71-126">Remarks</span></span>

<span data-ttu-id="96e71-127">Los elementos secundarios enumerados anteriormente se definen mediante los tipos de elementos complejos de [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="96e71-127">The child elements listed above are defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex element types.</span></span>

<span data-ttu-id="96e71-128">La hora del día en que se inicia la tarea se establece mediante el elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="96e71-128">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="96e71-129">Para el desarrollo de scripting, se especifica un desencadenador semanal mediante el objeto [**WeeklyTrigger**](weeklytrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="96e71-129">For scripting development, a weekly trigger is specified using the [**WeeklyTrigger**](weeklytrigger.md) object.</span></span>

<span data-ttu-id="96e71-130">En el desarrollo de C++, se especifica un desencadenador semanal mediante la interfaz [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) .</span><span class="sxs-lookup"><span data-stu-id="96e71-130">For C++ development, a weekly trigger is specified using the [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="96e71-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="96e71-131">Examples</span></span>

<span data-ttu-id="96e71-132">El siguiente código XML define un desencadenador de calendario semanal que inicia una tarea de lunes a viernes (a las 8:00 A.M.) cada semana.</span><span class="sxs-lookup"><span data-stu-id="96e71-132">The following XML defines a weekly calendar trigger that starts a task Monday through Friday (at 8:00 AM) every week.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByWeek>
        <WeeksInterval>1</WeeksInterval>
        <DaysOfWeek>
            <Monday/>
            <Tuesday/>
            <Wednesday/>
            <Thurday/>
            <Friday/>
        </DaysOfWeek>
    </ScheduleByWeek>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="96e71-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96e71-133">Requirements</span></span>



| <span data-ttu-id="96e71-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="96e71-134">Requirement</span></span> | <span data-ttu-id="96e71-135">Value</span><span class="sxs-lookup"><span data-stu-id="96e71-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="96e71-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96e71-136">Minimum supported client</span></span><br/> | <span data-ttu-id="96e71-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="96e71-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="96e71-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96e71-138">Minimum supported server</span></span><br/> | <span data-ttu-id="96e71-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="96e71-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96e71-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="96e71-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e71-141">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="96e71-141">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="96e71-142">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="96e71-142">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





