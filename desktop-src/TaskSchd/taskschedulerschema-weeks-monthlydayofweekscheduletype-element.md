---
title: Weeks (monthlyDayOfWeekScheduleType), elemento
description: Especifica las semanas del mes en que se ejecuta la tarea.
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- Elemento weeks Programador de tareas
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e032b936353d2c89a84b5da684f681ea3c2b6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803632"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a><span data-ttu-id="e7b09-104">Weeks (monthlyDayOfWeekScheduleType), elemento</span><span class="sxs-lookup"><span data-stu-id="e7b09-104">Weeks (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="e7b09-105">Especifica las semanas del mes en que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="e7b09-105">Specifies the weeks of the month in which the task is run.</span></span>

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

<span data-ttu-id="e7b09-106">El elemento **weeks** se define mediante el tipo complejo [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e7b09-106">The **Weeks** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e7b09-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="e7b09-107">Parent element</span></span>



| <span data-ttu-id="e7b09-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e7b09-108">Element</span></span>                                                                                                      | <span data-ttu-id="e7b09-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e7b09-109">Derived from</span></span>                                                                                         | <span data-ttu-id="e7b09-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7b09-110">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7b09-111">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="e7b09-111">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="e7b09-112">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="e7b09-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="e7b09-113">Especifica un desencadenador que inicia un trabajo en una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="e7b09-113">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="e7b09-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e7b09-114">Child elements</span></span>



| <span data-ttu-id="e7b09-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="e7b09-115">Element</span></span>                                                    | <span data-ttu-id="e7b09-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7b09-116">Type</span></span>                                                        | <span data-ttu-id="e7b09-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7b09-117">Description</span></span>                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="e7b09-118">**Semana**</span><span class="sxs-lookup"><span data-stu-id="e7b09-118">**Week**</span></span>](taskschedulerschema-week-weekstype-element.md) | [<span data-ttu-id="e7b09-119">**weekType**</span><span class="sxs-lookup"><span data-stu-id="e7b09-119">**weekType**</span></span>](taskschedulerschema-weektype-simpletype.md) | <span data-ttu-id="e7b09-120">Especifica una semana específica del mes.</span><span class="sxs-lookup"><span data-stu-id="e7b09-120">Specifies a specific week of the month.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e7b09-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7b09-121">Remarks</span></span>

<span data-ttu-id="e7b09-122">Para el desarrollo de scripting, las semanas del mes se especifican mediante la propiedad [**MonthlyDOWTrigger. WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) .</span><span class="sxs-lookup"><span data-stu-id="e7b09-122">For scripting development, the weeks of the month are specified using the [**MonthlyDOWTrigger.WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) property.</span></span>

<span data-ttu-id="e7b09-123">En el desarrollo de C++, las semanas del mes se especifican mediante la propiedad [**IMonthlyDOWTrigger:: WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) .</span><span class="sxs-lookup"><span data-stu-id="e7b09-123">For C++ development, the weeks of the month are specified using the [**IMonthlyDOWTrigger::WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) property.</span></span>

<span data-ttu-id="e7b09-124">Al especificar las semanas del mes, use 1-4 para especificar las cuatro primeras semanas del mes o use la cadena "Last" para indicar la última semana, independientemente de la semana en la que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="e7b09-124">When specifying the weeks of the month, use 1-4 to specify the first four weeks of the month or use the string "Last" to indicate the last week regardless of which week it is.</span></span>

## <a name="examples"></a><span data-ttu-id="e7b09-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e7b09-125">Examples</span></span>

<span data-ttu-id="e7b09-126">El siguiente código XML define un calendario mensual de día de la semana que inicia la tarea el lunes de la primera semana para cada mes del año.</span><span class="sxs-lookup"><span data-stu-id="e7b09-126">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


```XML
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
```



## <a name="requirements"></a><span data-ttu-id="e7b09-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7b09-127">Requirements</span></span>



| <span data-ttu-id="e7b09-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b09-128">Requirement</span></span> | <span data-ttu-id="e7b09-129">Value</span><span class="sxs-lookup"><span data-stu-id="e7b09-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e7b09-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7b09-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e7b09-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e7b09-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e7b09-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7b09-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e7b09-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7b09-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7b09-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7b09-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b09-135">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="e7b09-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e7b09-136">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="e7b09-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





