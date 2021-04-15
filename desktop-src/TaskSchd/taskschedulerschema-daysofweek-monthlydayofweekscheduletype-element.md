---
title: DaysOfWeek (monthlyDayOfWeekScheduleType), elemento
description: Especifica los días de la semana en los que se ejecuta la tarea. | DaysOfWeek (monthlyDayOfWeekScheduleType), elemento
ms.assetid: d84f0019-1369-465f-9054-0fb5a83cad6d
keywords:
- Elemento DaysOfWeek Programador de tareas
topic_type:
- apiref
api_name:
- DaysOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3867e08dd001a035a3ab25da056f75c1e73eeeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689831"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a><span data-ttu-id="a8b1c-105">DaysOfWeek (monthlyDayOfWeekScheduleType), elemento</span><span class="sxs-lookup"><span data-stu-id="a8b1c-105">DaysOfWeek (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="a8b1c-106">Especifica los días de la semana en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-106">Specifies the days of the week in which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

<span data-ttu-id="a8b1c-107">El elemento **DaysOfWeek** se define mediante el tipo complejo de [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a8b1c-107">The **DaysOfWeek** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a8b1c-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="a8b1c-108">Parent element</span></span>



| <span data-ttu-id="a8b1c-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8b1c-109">Element</span></span>                                                                                                      | <span data-ttu-id="a8b1c-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="a8b1c-110">Derived from</span></span>                                                                                         | <span data-ttu-id="a8b1c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8b1c-111">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8b1c-112">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-112">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="a8b1c-113">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-113">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="a8b1c-114">Especifica un desencadenador que inicia un trabajo para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-114">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="a8b1c-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a8b1c-115">Child elements</span></span>



| <span data-ttu-id="a8b1c-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8b1c-116">Element</span></span>                                                                   | <span data-ttu-id="a8b1c-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8b1c-117">Type</span></span> | <span data-ttu-id="a8b1c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8b1c-118">Description</span></span>                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="a8b1c-119">**Día**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-119">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       |      | <span data-ttu-id="a8b1c-120">Especifica que la tarea se ejecuta el viernes.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-120">Specifies that the task runs on Friday.</span></span><br/>    |
| [<span data-ttu-id="a8b1c-121">**Lunes**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-121">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       |      | <span data-ttu-id="a8b1c-122">Especifica que la tarea se ejecuta el lunes.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-122">Specifies that the task runs on Monday.</span></span><br/>    |
| [<span data-ttu-id="a8b1c-123">**Sábado**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-123">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   |      | <span data-ttu-id="a8b1c-124">Especifica que la tarea se ejecuta el sábado.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-124">Specifies that the task runs on Saturday.</span></span><br/>  |
| [<span data-ttu-id="a8b1c-125">**Domingo**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-125">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       |      | <span data-ttu-id="a8b1c-126">Especifica que la tarea se ejecuta el domingo.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-126">Specifies that the task runs on Sunday.</span></span><br/>    |
| [<span data-ttu-id="a8b1c-127">**Martes**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-127">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   |      | <span data-ttu-id="a8b1c-128">Especifica que la tarea se ejecuta el jueves.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-128">Specifies that the task runs on Thursday.</span></span><br/>  |
| [<span data-ttu-id="a8b1c-129">**Jueves**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-129">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | <span data-ttu-id="a8b1c-130">Especifica que la tarea se ejecuta el martes.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-130">Specifies that the task runs on Tuesday.</span></span><br/>   |
| [<span data-ttu-id="a8b1c-131">**Lunes**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-131">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) |      | <span data-ttu-id="a8b1c-132">Especifica que la tarea se ejecuta el miércoles.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-132">Specifies that the task runs on Wednesday.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a8b1c-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8b1c-133">Remarks</span></span>

<span data-ttu-id="a8b1c-134">Para el desarrollo de scripting, los días de la semana de un calendario mensual de día de la semana se especifican mediante la propiedad [**MonthlyDOWTrigger. DaysOfWeek**](monthlydowtrigger-daysofweek.md) .</span><span class="sxs-lookup"><span data-stu-id="a8b1c-134">For scripting development, the days of the week for a monthly day-of-week calendar are specified using the [**MonthlyDOWTrigger.DaysOfWeek**](monthlydowtrigger-daysofweek.md) property.</span></span>

<span data-ttu-id="a8b1c-135">En el desarrollo de C++, los días de la semana de un calendario mensual de día de la semana se especifican mediante la propiedad [**IMonthlyDOWTrigger::D aysofweek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) .</span><span class="sxs-lookup"><span data-stu-id="a8b1c-135">For C++ development, the days of the week for a monthly day-of-week calendar are specified using the [**IMonthlyDOWTrigger::DaysOfWeek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) property.</span></span>

<span data-ttu-id="a8b1c-136">Los elementos secundarios anteriores se definen mediante el tipo complejo de [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a8b1c-136">The child elements above are defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="examples"></a><span data-ttu-id="a8b1c-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a8b1c-137">Examples</span></span>

<span data-ttu-id="a8b1c-138">El siguiente código XML define un calendario mensual de día de la semana que inicia la tarea el lunes de la primera semana para cada mes del año.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-138">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a8b1c-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8b1c-139">Requirements</span></span>



| <span data-ttu-id="a8b1c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8b1c-140">Requirement</span></span> | <span data-ttu-id="a8b1c-141">Value</span><span class="sxs-lookup"><span data-stu-id="a8b1c-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8b1c-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8b1c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b1c-143">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a8b1c-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8b1c-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8b1c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b1c-145">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8b1c-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8b1c-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8b1c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b1c-147">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="a8b1c-147">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a8b1c-148">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="a8b1c-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





