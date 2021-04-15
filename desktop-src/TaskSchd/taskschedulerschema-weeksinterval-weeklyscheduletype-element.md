---
title: Elemento WeeksInterval (weeklyScheduleType)
description: Especifica el intervalo entre las semanas de la programación.
ms.assetid: 6cbf1e7e-a695-4012-97fd-fe3360c362c4
keywords:
- Programador de tareas del elemento WeeksInterval
topic_type:
- apiref
api_name:
- WeeksInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 747ca4b73ff18bdb3e29d8b909d72b8d2367d89b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422534"
---
# <a name="weeksinterval-weeklyscheduletype-element"></a><span data-ttu-id="b9fab-104">Elemento WeeksInterval (weeklyScheduleType)</span><span class="sxs-lookup"><span data-stu-id="b9fab-104">WeeksInterval (weeklyScheduleType) Element</span></span>

<span data-ttu-id="b9fab-105">Especifica el intervalo entre las semanas de la programación.</span><span class="sxs-lookup"><span data-stu-id="b9fab-105">Specifies the interval between the weeks in the schedule.</span></span>

``` syntax
<xs:element name="WeeksInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="52"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="b9fab-106">El elemento se define mediante el tipo complejo de [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b9fab-106">The element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b9fab-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="b9fab-107">Parent element</span></span>



| <span data-ttu-id="b9fab-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b9fab-108">Element</span></span>                                                                                  | <span data-ttu-id="b9fab-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="b9fab-109">Derived from</span></span>                                                                     | <span data-ttu-id="b9fab-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9fab-110">Description</span></span>                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="b9fab-111">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="b9fab-111">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [<span data-ttu-id="b9fab-112">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="b9fab-112">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md) | <span data-ttu-id="b9fab-113">Especifica una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="b9fab-113">Specifies a weekly schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b9fab-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9fab-114">Remarks</span></span>

<span data-ttu-id="b9fab-115">Para el desarrollo de scripting, el intervalo semanal se especifica mediante la propiedad [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="b9fab-115">For scripting development, the weekly interval is specified using the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md) property.</span></span>

<span data-ttu-id="b9fab-116">En el desarrollo de C++, el intervalo semanal se especifica mediante la propiedad [**IWeeklyTrigger:: WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .</span><span class="sxs-lookup"><span data-stu-id="b9fab-116">For C++ development, the weekly interval is specified using the [**IWeeklyTrigger::WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="b9fab-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b9fab-117">Examples</span></span>

<span data-ttu-id="b9fab-118">El siguiente código XML define un desencadenador de calendario semanal que inicia una tarea de lunes a viernes (a las 8:00 A.M.) cada semana.</span><span class="sxs-lookup"><span data-stu-id="b9fab-118">The following XML defines a weekly calendar trigger that starts a task Monday through Friday ( at 8:00 AM) every week.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b9fab-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9fab-119">Requirements</span></span>



| <span data-ttu-id="b9fab-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9fab-120">Requirement</span></span> | <span data-ttu-id="b9fab-121">Value</span><span class="sxs-lookup"><span data-stu-id="b9fab-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b9fab-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9fab-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b9fab-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b9fab-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b9fab-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9fab-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b9fab-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9fab-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b9fab-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9fab-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9fab-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="b9fab-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b9fab-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="b9fab-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





