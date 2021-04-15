---
title: Months (monthlyDayOfWeekScheduleType), elemento
description: Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Months, elemento Programador de tareas
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76f13a5823e0154519dbdb093dd03ea36bbe77b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422095"
---
# <a name="months-monthlydayofweekscheduletype-element"></a><span data-ttu-id="8c565-104">Months (monthlyDayOfWeekScheduleType), elemento</span><span class="sxs-lookup"><span data-stu-id="8c565-104">Months (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="8c565-105">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="8c565-105">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span>

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

<span data-ttu-id="8c565-106">El elemento **months** se define mediante el tipo complejo [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8c565-106">The **Months** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8c565-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="8c565-107">Parent element</span></span>



| <span data-ttu-id="8c565-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="8c565-108">Element</span></span>                                                                                                                            | <span data-ttu-id="8c565-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="8c565-109">Derived from</span></span>                                                                                         | <span data-ttu-id="8c565-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c565-110">Description</span></span>                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c565-111">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="8c565-111">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="8c565-112">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="8c565-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="8c565-113">Especifica un desencadenador que inicia un trabajo para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="8c565-113">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="8c565-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8c565-114">Child elements</span></span>



| <span data-ttu-id="8c565-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="8c565-115">Element</span></span>                                                               | <span data-ttu-id="8c565-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c565-116">Type</span></span> | <span data-ttu-id="8c565-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c565-117">Description</span></span>                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="8c565-118">**April**</span><span class="sxs-lookup"><span data-stu-id="8c565-118">**April**</span></span>](taskschedulerschema-april-monthstype-element.md)         |      | <span data-ttu-id="8c565-119">Especifica que la tarea se ejecuta en abril.</span><span class="sxs-lookup"><span data-stu-id="8c565-119">Specifies that the task runs in April.</span></span><br/>     |
| [<span data-ttu-id="8c565-120">**Agosto**</span><span class="sxs-lookup"><span data-stu-id="8c565-120">**August**</span></span>](taskschedulerschema-august-monthstype-element.md)       |      | <span data-ttu-id="8c565-121">Especifica que la tarea se ejecuta en agosto.</span><span class="sxs-lookup"><span data-stu-id="8c565-121">Specifies that the task runs in August.</span></span><br/>    |
| [<span data-ttu-id="8c565-122">**Diciembre**</span><span class="sxs-lookup"><span data-stu-id="8c565-122">**December**</span></span>](taskschedulerschema-december-monthstype-element.md)   |      | <span data-ttu-id="8c565-123">Especifica que la tarea se ejecuta en diciembre.</span><span class="sxs-lookup"><span data-stu-id="8c565-123">Specifies that the task runs in December.</span></span><br/>  |
| [<span data-ttu-id="8c565-124">**February**</span><span class="sxs-lookup"><span data-stu-id="8c565-124">**February**</span></span>](taskschedulerschema-february-monthstype-element.md)   |      | <span data-ttu-id="8c565-125">Especifica que la tarea se ejecuta en febrero.</span><span class="sxs-lookup"><span data-stu-id="8c565-125">Specifies that the task runs in February.</span></span><br/>  |
| [<span data-ttu-id="8c565-126">**January**</span><span class="sxs-lookup"><span data-stu-id="8c565-126">**January**</span></span>](taskschedulerschema-january-monthstype-element.md)     |      | <span data-ttu-id="8c565-127">Especifica que la tarea se ejecuta en enero.</span><span class="sxs-lookup"><span data-stu-id="8c565-127">Specifies that the task runs in January.</span></span><br/>   |
| [<span data-ttu-id="8c565-128">**Julio**</span><span class="sxs-lookup"><span data-stu-id="8c565-128">**July**</span></span>](taskschedulerschema-july-monthstype-element.md)           |      | <span data-ttu-id="8c565-129">Especifica que la tarea se ejecuta en julio.</span><span class="sxs-lookup"><span data-stu-id="8c565-129">Specifies that the task runs in July.</span></span><br/>      |
| [<span data-ttu-id="8c565-130">**Junio**</span><span class="sxs-lookup"><span data-stu-id="8c565-130">**June**</span></span>](taskschedulerschema-june-monthstype-element.md)           |      | <span data-ttu-id="8c565-131">Especifica que la tarea se ejecuta en junio.</span><span class="sxs-lookup"><span data-stu-id="8c565-131">Specifies that the task runs in June.</span></span><br/>      |
| [<span data-ttu-id="8c565-132">**Marzo**</span><span class="sxs-lookup"><span data-stu-id="8c565-132">**March**</span></span>](taskschedulerschema-march-monthstype-element.md)         |      | <span data-ttu-id="8c565-133">Especifica que la tarea se ejecuta en marzo.</span><span class="sxs-lookup"><span data-stu-id="8c565-133">Specifies that the task runs in March.</span></span><br/>     |
| [<span data-ttu-id="8c565-134">**May**</span><span class="sxs-lookup"><span data-stu-id="8c565-134">**May**</span></span>](taskschedulerschema-may-monthstype-element.md)             |      | <span data-ttu-id="8c565-135">Especifica que la tarea se ejecuta en mayo.</span><span class="sxs-lookup"><span data-stu-id="8c565-135">Specifies that the task runs in May.</span></span><br/>       |
| [<span data-ttu-id="8c565-136">**Noviembre**</span><span class="sxs-lookup"><span data-stu-id="8c565-136">**November**</span></span>](taskschedulerschema-november-monthstype-element.md)   |      | <span data-ttu-id="8c565-137">Especifica que la tarea se ejecuta en noviembre.</span><span class="sxs-lookup"><span data-stu-id="8c565-137">Specifies that the task runs in November.</span></span><br/>  |
| [<span data-ttu-id="8c565-138">**Octubre**</span><span class="sxs-lookup"><span data-stu-id="8c565-138">**October**</span></span>](taskschedulerschema-october-monthstype-element.md)     |      | <span data-ttu-id="8c565-139">Especifica que la tarea se ejecuta en octubre.</span><span class="sxs-lookup"><span data-stu-id="8c565-139">Specifies that the task runs in October.</span></span><br/>   |
| [<span data-ttu-id="8c565-140">**Septiembre**</span><span class="sxs-lookup"><span data-stu-id="8c565-140">**September**</span></span>](taskschedulerschema-september-monthstype-element.md) |      | <span data-ttu-id="8c565-141">Especifica que la tarea se ejecuta en septiembre.</span><span class="sxs-lookup"><span data-stu-id="8c565-141">Specifies that the task runs in September.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8c565-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c565-142">Remarks</span></span>

<span data-ttu-id="8c565-143">Para el desarrollo de scripting, los meses de un año para una programación mensual de día de la semana se especifican mediante la propiedad [**MonthlyDOWTrigger. MonthsOfYear**](monthlydowtrigger-monthsofyear.md) .</span><span class="sxs-lookup"><span data-stu-id="8c565-143">For scripting development, the months of a year for a monthly day-of-week schedule are specified using the [**MonthlyDOWTrigger.MonthsOfYear**](monthlydowtrigger-monthsofyear.md) property.</span></span>

<span data-ttu-id="8c565-144">En el desarrollo de C++, los meses de un año para una programación mensual de día de la semana se especifican mediante la propiedad [**IMonthlyDOWTrigger:: MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) .</span><span class="sxs-lookup"><span data-stu-id="8c565-144">For C++ development, the months of a year for a monthly day-of-week schedule are specified using the [**IMonthlyDOWTrigger::MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) property.</span></span>

<span data-ttu-id="8c565-145">Los elementos secundarios anteriores se definen mediante el tipo complejo de [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8c565-145">The child elements above are defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="examples"></a><span data-ttu-id="8c565-146">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8c565-146">Examples</span></span>

<span data-ttu-id="8c565-147">El siguiente código XML define un calendario mensual de día de la semana que inicia la tarea el lunes de la primera semana para cada mes del año.</span><span class="sxs-lookup"><span data-stu-id="8c565-147">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8c565-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c565-148">Requirements</span></span>



| <span data-ttu-id="8c565-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c565-149">Requirement</span></span> | <span data-ttu-id="8c565-150">Value</span><span class="sxs-lookup"><span data-stu-id="8c565-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8c565-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c565-151">Minimum supported client</span></span><br/> | <span data-ttu-id="8c565-152">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8c565-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8c565-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c565-153">Minimum supported server</span></span><br/> | <span data-ttu-id="8c565-154">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c565-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c565-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c565-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c565-156">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="8c565-156">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="8c565-157">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="8c565-157">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





