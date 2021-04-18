---
title: Elemento DaysOfMonth (monthlyScheduleType)
description: Especifica los días del mes durante los que se ejecuta la tarea.
ms.assetid: 62f28f44-b3d8-414e-80d4-f4d8bd3c4527
keywords:
- Programador de tareas del elemento DaysOfMonth
topic_type:
- apiref
api_name:
- DaysOfMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38c2106f8d612ee27dc1297023a59b531fa9548d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686234"
---
# <a name="daysofmonth-monthlyscheduletype-element"></a><span data-ttu-id="f556a-104">Elemento DaysOfMonth (monthlyScheduleType)</span><span class="sxs-lookup"><span data-stu-id="f556a-104">DaysOfMonth (monthlyScheduleType) Element</span></span>

<span data-ttu-id="f556a-105">Especifica los días del mes durante los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="f556a-105">Specifies the days of the month during which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfMonth"
    type="daysOfMonthType"
 />
```

<span data-ttu-id="f556a-106">El elemento **DaysOfMonth** se define mediante el tipo complejo de [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f556a-106">The **DaysOfMonth** element is defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f556a-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="f556a-107">Parent element</span></span>



| <span data-ttu-id="f556a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f556a-108">Element</span></span>                                                                                    | <span data-ttu-id="f556a-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f556a-109">Derived from</span></span>                                                                                         | <span data-ttu-id="f556a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f556a-110">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="f556a-111">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="f556a-111">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [<span data-ttu-id="f556a-112">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="f556a-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="f556a-113">Especifica un desencadenador que inicia un trabajo para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="f556a-113">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f556a-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f556a-114">Child elements</span></span>



| <span data-ttu-id="f556a-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="f556a-115">Element</span></span>                                                        | <span data-ttu-id="f556a-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="f556a-116">Type</span></span>                                                                    | <span data-ttu-id="f556a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f556a-117">Description</span></span>                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="f556a-118">**Diariamente**</span><span class="sxs-lookup"><span data-stu-id="f556a-118">**Day**</span></span>](taskschedulerschema-day-daysofmonthtype-element.md) | [<span data-ttu-id="f556a-119">**dayOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="f556a-119">**dayOfMonthType**</span></span>](taskschedulerschema-dayofmonthtype-simpletype.md) | <span data-ttu-id="f556a-120">Especifica un día del mes durante el que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="f556a-120">Specifies a day of the month during which the task runs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f556a-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f556a-121">Remarks</span></span>

<span data-ttu-id="f556a-122">Para el desarrollo de scripts, los días del mes para la programación se especifican mediante la propiedad [**MonthlyTrigger. DaysOfMonth**](monthlytrigger-daysofmonth.md) .</span><span class="sxs-lookup"><span data-stu-id="f556a-122">For script development, the days of the month for the schedule are specified using the [**MonthlyTrigger.DaysOfMonth**](monthlytrigger-daysofmonth.md) property.</span></span>

<span data-ttu-id="f556a-123">En el desarrollo de C++, los días del mes para la programación se especifican mediante la propiedad [**IMonthlyTrigger::D aysofmonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) .</span><span class="sxs-lookup"><span data-stu-id="f556a-123">For C++ development, the days of the month for the schedule are specified using the [**IMonthlyTrigger::DaysOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) property.</span></span>

<span data-ttu-id="f556a-124">El elemento secundario se debe repetir para cada día del mes en el que se va a ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="f556a-124">The child element must be repeated for each day of the month the task is to run.</span></span>

## <a name="examples"></a><span data-ttu-id="f556a-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f556a-125">Examples</span></span>

<span data-ttu-id="f556a-126">El siguiente código XML define un desencadenador de calendario mensual que inicia una tarea (a las 8:30 A.M.) el día 1 de cada mes.</span><span class="sxs-lookup"><span data-stu-id="f556a-126">The following XML defines a monthly calendar trigger that starts a task (at 8:30 AM) on the 1st day of every month.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>  
        </DaysOfMonth>
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
    </ScheduleByMonth>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="f556a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f556a-127">Requirements</span></span>



| <span data-ttu-id="f556a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f556a-128">Requirement</span></span> | <span data-ttu-id="f556a-129">Value</span><span class="sxs-lookup"><span data-stu-id="f556a-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f556a-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f556a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f556a-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f556a-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f556a-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f556a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f556a-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f556a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f556a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f556a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f556a-135">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="f556a-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f556a-136">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f556a-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





