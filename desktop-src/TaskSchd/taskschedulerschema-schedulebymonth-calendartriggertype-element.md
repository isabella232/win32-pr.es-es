---
title: Elemento ScheduleByMonth (calendarTriggerType)
description: Especifica una programación mensual.
ms.assetid: 3a23f4d0-bdaf-4f2a-81c6-8652a0849fc8
keywords:
- Programador de tareas del elemento ScheduleByMonth
topic_type:
- apiref
api_name:
- ScheduleByMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6fda84a1cd4373f7988fa66a5ad70c97dd371d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150846"
---
# <a name="schedulebymonth-calendartriggertype-element"></a><span data-ttu-id="94e88-104">Elemento ScheduleByMonth (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="94e88-104">ScheduleByMonth (calendarTriggerType) Element</span></span>

<span data-ttu-id="94e88-105">Especifica una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="94e88-105">Specifies a monthly schedule.</span></span> <span data-ttu-id="94e88-106">Por ejemplo, la tarea comienza a las 8:00 AM en días específicos del mes en meses específicos.</span><span class="sxs-lookup"><span data-stu-id="94e88-106">For example, the task starts at 8:00 AM on specific days of the month on specific months.</span></span>

``` syntax
<xs:element name="ScheduleByMonth"
    type="monthlyScheduleType"
 />
```

<span data-ttu-id="94e88-107">El elemento **ScheduleByMonth** se define mediante el tipo complejo de [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="94e88-107">The **ScheduleByMonth** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="94e88-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="94e88-108">Parent element</span></span>



| <span data-ttu-id="94e88-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="94e88-109">Element</span></span>                                                                             | <span data-ttu-id="94e88-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="94e88-110">Derived from</span></span>                                                                       | <span data-ttu-id="94e88-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="94e88-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94e88-112">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="94e88-112">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="94e88-113">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="94e88-113">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="94e88-114">Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.</span><span class="sxs-lookup"><span data-stu-id="94e88-114">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="94e88-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="94e88-115">Child elements</span></span>



| <span data-ttu-id="94e88-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="94e88-116">Element</span></span>                                                                                                  | <span data-ttu-id="94e88-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="94e88-117">Type</span></span>                                                                       | <span data-ttu-id="94e88-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="94e88-118">Description</span></span>                                                             |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="94e88-119">**DaysOfMonth (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="94e88-119">**DaysOfMonth (monthlyScheduleType)**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="94e88-120">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="94e88-120">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="94e88-121">Especifica los días del mes durante los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="94e88-121">Specifies the days of the month during which the task runs.</span></span><br/>  |
| [<span data-ttu-id="94e88-122">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="94e88-122">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)           | [<span data-ttu-id="94e88-123">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="94e88-123">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)           | <span data-ttu-id="94e88-124">Especifica los meses del año en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="94e88-124">Specifies the months of the year during which the task runs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="94e88-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94e88-125">Remarks</span></span>

<span data-ttu-id="94e88-126">La hora del día en que se inicia la tarea se establece mediante el elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="94e88-126">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="94e88-127">Para el desarrollo de scripts, se especifica un desencadenador mensual mediante el objeto [**MonthlyTrigger**](monthlytrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="94e88-127">For script development, a monthly trigger is specified using the [**MonthlyTrigger**](monthlytrigger.md) object.</span></span>

<span data-ttu-id="94e88-128">En el desarrollo de C++, se especifica un desencadenador mensual mediante la interfaz [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) .</span><span class="sxs-lookup"><span data-stu-id="94e88-128">For C++ development, a monthly trigger is specified using the [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) interface.</span></span>

<span data-ttu-id="94e88-129">Los elementos secundarios que se enumeran a continuación se definen mediante los tipos de elementos complejos de [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="94e88-129">The child elements listed below are defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex element types.</span></span>

## <a name="examples"></a><span data-ttu-id="94e88-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="94e88-130">Examples</span></span>

<span data-ttu-id="94e88-131">El siguiente código XML define un desencadenador de calendario mensual que inicia una tarea (a las 8:00 A.M.) el día 1 y el 15 de cada mes del año.</span><span class="sxs-lookup"><span data-stu-id="94e88-131">The following XML defines a monthly calendar trigger that starts a task ( at 8:00 AM) on the 1st and 15th day of every month of the year.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>
            <Day>15</Day>
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
        </Months>
    </ScheduleByMonth>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="94e88-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94e88-132">Requirements</span></span>



| <span data-ttu-id="94e88-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="94e88-133">Requirement</span></span> | <span data-ttu-id="94e88-134">Value</span><span class="sxs-lookup"><span data-stu-id="94e88-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="94e88-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94e88-135">Minimum supported client</span></span><br/> | <span data-ttu-id="94e88-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="94e88-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="94e88-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94e88-137">Minimum supported server</span></span><br/> | <span data-ttu-id="94e88-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="94e88-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94e88-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="94e88-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94e88-140">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="94e88-140">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="94e88-141">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="94e88-141">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





