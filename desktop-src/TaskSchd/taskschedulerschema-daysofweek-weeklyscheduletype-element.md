---
title: DaysOfWeek (weeklyScheduleType), elemento
description: Especifica los días de la semana en los que se ejecuta la tarea. | DaysOfWeek (weeklyScheduleType), elemento
ms.assetid: 86555681-2324-4095-9eab-fdef40e0acba
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
ms.openlocfilehash: 3a2b310feb49f3141d1f7f08c4552305f9ffc3ea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689830"
---
# <a name="daysofweek-weeklyscheduletype-element"></a><span data-ttu-id="96843-105">DaysOfWeek (weeklyScheduleType), elemento</span><span class="sxs-lookup"><span data-stu-id="96843-105">DaysOfWeek (weeklyScheduleType) Element</span></span>

<span data-ttu-id="96843-106">Especifica los días de la semana en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="96843-106">Specifies the days of the week in which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

<span data-ttu-id="96843-107">El elemento **DaysOfWeek** se define mediante el tipo complejo de [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="96843-107">The **DaysOfWeek** element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="96843-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="96843-108">Parent element</span></span>



| <span data-ttu-id="96843-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="96843-109">Element</span></span>                                                                                  | <span data-ttu-id="96843-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="96843-110">Derived from</span></span>                                                                     | <span data-ttu-id="96843-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="96843-111">Description</span></span>                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="96843-112">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="96843-112">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [<span data-ttu-id="96843-113">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="96843-113">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md) | <span data-ttu-id="96843-114">Especifica una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="96843-114">Specifies a weekly schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="96843-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="96843-115">Child elements</span></span>



| <span data-ttu-id="96843-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="96843-116">Element</span></span>                                                                   | <span data-ttu-id="96843-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="96843-117">Type</span></span> | <span data-ttu-id="96843-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="96843-118">Description</span></span>                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="96843-119">**Día**</span><span class="sxs-lookup"><span data-stu-id="96843-119">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       |      | <span data-ttu-id="96843-120">Especifica que la tarea se ejecuta el viernes.</span><span class="sxs-lookup"><span data-stu-id="96843-120">Specifies that the task runs on Friday.</span></span><br/>    |
| [<span data-ttu-id="96843-121">**Lunes**</span><span class="sxs-lookup"><span data-stu-id="96843-121">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       |      | <span data-ttu-id="96843-122">Especifica que la tarea se ejecuta el lunes.</span><span class="sxs-lookup"><span data-stu-id="96843-122">Specifies that the task runs on Monday.</span></span><br/>    |
| [<span data-ttu-id="96843-123">**Sábado**</span><span class="sxs-lookup"><span data-stu-id="96843-123">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   |      | <span data-ttu-id="96843-124">Especifica que la tarea se ejecuta el sábado.</span><span class="sxs-lookup"><span data-stu-id="96843-124">Specifies that the task runs on Saturday.</span></span><br/>  |
| [<span data-ttu-id="96843-125">**Domingo**</span><span class="sxs-lookup"><span data-stu-id="96843-125">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       |      | <span data-ttu-id="96843-126">Especifica que la tarea se ejecuta el domingo.</span><span class="sxs-lookup"><span data-stu-id="96843-126">Specifies that the task runs on Sunday.</span></span><br/>    |
| [<span data-ttu-id="96843-127">**Martes**</span><span class="sxs-lookup"><span data-stu-id="96843-127">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   |      | <span data-ttu-id="96843-128">Especifica que la tarea se ejecuta el jueves.</span><span class="sxs-lookup"><span data-stu-id="96843-128">Specifies that the task runs on Thursday.</span></span><br/>  |
| [<span data-ttu-id="96843-129">**Jueves**</span><span class="sxs-lookup"><span data-stu-id="96843-129">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | <span data-ttu-id="96843-130">Especifica que la tarea se ejecuta el martes.</span><span class="sxs-lookup"><span data-stu-id="96843-130">Specifies that the task runs on Tuesday.</span></span><br/>   |
| [<span data-ttu-id="96843-131">**Lunes**</span><span class="sxs-lookup"><span data-stu-id="96843-131">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) |      | <span data-ttu-id="96843-132">Especifica que la tarea se ejecuta el miércoles.</span><span class="sxs-lookup"><span data-stu-id="96843-132">Specifies that the task runs on Wednesday.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="96843-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96843-133">Remarks</span></span>

<span data-ttu-id="96843-134">Los elementos secundarios anteriores se definen mediante el tipo complejo de [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="96843-134">The previous child elements are defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

<span data-ttu-id="96843-135">Para el desarrollo de scripting, el intervalo semanal se especifica mediante la propiedad [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="96843-135">For scripting development, the weekly interval is specified using the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md) property.</span></span>

<span data-ttu-id="96843-136">En el desarrollo de C++, el intervalo semanal se especifica mediante la propiedad [**IWeeklyTrigger:: WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .</span><span class="sxs-lookup"><span data-stu-id="96843-136">For C++ development, the weekly interval is specified using the [**IWeeklyTrigger::WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="96843-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="96843-137">Examples</span></span>

<span data-ttu-id="96843-138">El siguiente código XML define un desencadenador de calendario diario que inicia una tarea de lunes a viernes (a las 8:00 A.M.) cada semana.</span><span class="sxs-lookup"><span data-stu-id="96843-138">The following XML defines a daily calendar trigger that starts a task Monday through Friday ( at 8:00 AM) every week.</span></span>


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



<span data-ttu-id="96843-139">Para obtener un ejemplo completo del XML de una tarea que utiliza un desencadenador semanal, consulte el [ejemplo de desencadenador semanal (XML)](weekly-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="96843-139">For a complete example of the XML for a task that uses a weekly trigger, see [Weekly Trigger Example (XML)](weekly-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="96843-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96843-140">Requirements</span></span>



| <span data-ttu-id="96843-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="96843-141">Requirement</span></span> | <span data-ttu-id="96843-142">Value</span><span class="sxs-lookup"><span data-stu-id="96843-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="96843-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96843-143">Minimum supported client</span></span><br/> | <span data-ttu-id="96843-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="96843-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="96843-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96843-145">Minimum supported server</span></span><br/> | <span data-ttu-id="96843-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="96843-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96843-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="96843-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96843-148">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="96843-148">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="96843-149">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="96843-149">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





