---
title: Elemento ScheduleByDay (calendarTriggerType)
description: Especifica una programación diaria.
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- Programador de tareas de desencadenador diario, elemento XML
- Programador de tareas del elemento ScheduleByDay
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 614777ede63605dc7ed6936bda952c6071bda371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996882"
---
# <a name="schedulebyday-calendartriggertype-element"></a><span data-ttu-id="96fe4-105">Elemento ScheduleByDay (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="96fe4-105">ScheduleByDay (calendarTriggerType) Element</span></span>

<span data-ttu-id="96fe4-106">Especifica una programación diaria.</span><span class="sxs-lookup"><span data-stu-id="96fe4-106">Specifies a daily schedule.</span></span> <span data-ttu-id="96fe4-107">Por ejemplo, la tarea comienza a las 8:00 A.M. todos los días, cada día, cada tres días, etc.</span><span class="sxs-lookup"><span data-stu-id="96fe4-107">For example, the task starts at 8:00 AM every day, every-other day, every third day, and so on.</span></span>

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

<span data-ttu-id="96fe4-108">El elemento **ScheduleByDay** se define mediante el tipo complejo de [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="96fe4-108">The **ScheduleByDay** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="96fe4-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="96fe4-109">Parent element</span></span>



| <span data-ttu-id="96fe4-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="96fe4-110">Element</span></span>                                                                             | <span data-ttu-id="96fe4-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="96fe4-111">Derived from</span></span>                                                                       | <span data-ttu-id="96fe4-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="96fe4-112">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96fe4-113">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="96fe4-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="96fe4-114">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="96fe4-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="96fe4-115">Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.</span><span class="sxs-lookup"><span data-stu-id="96fe4-115">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="96fe4-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="96fe4-116">Child elements</span></span>



| <span data-ttu-id="96fe4-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="96fe4-117">Element</span></span>                                                                            | <span data-ttu-id="96fe4-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="96fe4-118">Type</span></span>             | <span data-ttu-id="96fe4-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="96fe4-119">Description</span></span>                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="96fe4-120">**DaysInterval**</span><span class="sxs-lookup"><span data-stu-id="96fe4-120">**DaysInterval**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | <span data-ttu-id="96fe4-121">**unsignedByte**</span><span class="sxs-lookup"><span data-stu-id="96fe4-121">**unsignedByte**</span></span> | <span data-ttu-id="96fe4-122">Especifica el intervalo entre los días de la programación.</span><span class="sxs-lookup"><span data-stu-id="96fe4-122">Specifies the interval between the days in the schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="96fe4-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96fe4-123">Remarks</span></span>

<span data-ttu-id="96fe4-124">El elemento secundario enumerado anteriormente está definido por los tipos de elemento complejo [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="96fe4-124">The child element listed previously is defined by the [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) complex element types.</span></span>

<span data-ttu-id="96fe4-125">La hora del día en que se inicia la tarea se establece mediante el elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="96fe4-125">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="96fe4-126">Para el desarrollo de scripting, se especifica un desencadenador diario mediante el objeto [**DailyTrigger**](weeklytrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="96fe4-126">For scripting development, a daily trigger is specified using the [**DailyTrigger**](weeklytrigger.md) object.</span></span>

<span data-ttu-id="96fe4-127">En el desarrollo de C++, se especifica un desencadenador diario mediante la interfaz [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) .</span><span class="sxs-lookup"><span data-stu-id="96fe4-127">For C++ development, a daily trigger is specified using the [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="96fe4-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="96fe4-128">Examples</span></span>

<span data-ttu-id="96fe4-129">En el código XML siguiente se define un desencadenador de calendario diario que inicia la tarea cada día.</span><span class="sxs-lookup"><span data-stu-id="96fe4-129">The following XML defines a daily calendar trigger that starts the task every day.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



<span data-ttu-id="96fe4-130">Para obtener un ejemplo completo del XML de una tarea que especifica una programación diaria, vea [ejemplo de desencadenador diario (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="96fe4-130">For a complete example of the XML for a task that specifies a daily schedule, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="96fe4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96fe4-131">Requirements</span></span>



| <span data-ttu-id="96fe4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="96fe4-132">Requirement</span></span> | <span data-ttu-id="96fe4-133">Value</span><span class="sxs-lookup"><span data-stu-id="96fe4-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="96fe4-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96fe4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="96fe4-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="96fe4-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="96fe4-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96fe4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="96fe4-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="96fe4-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96fe4-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="96fe4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96fe4-139">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="96fe4-139">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="96fe4-140">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="96fe4-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





