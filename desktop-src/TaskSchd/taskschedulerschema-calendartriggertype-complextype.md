---
title: Tipo complejo de calendarTriggerType
description: Define los elementos secundarios y la información de secuenciación para los elementos de calendario.
ms.assetid: bf0d964e-aff2-4807-b086-c504f8963663
keywords:
- tipo complejo de calendarTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- calendarTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f45434fa68b6300157a29318ba257f43bac5992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676852"
---
# <a name="calendartriggertype-complex-type"></a><span data-ttu-id="f68ee-104">Tipo complejo de calendarTriggerType</span><span class="sxs-lookup"><span data-stu-id="f68ee-104">calendarTriggerType Complex Type</span></span>

<span data-ttu-id="f68ee-105">Define los elementos secundarios y la información de secuenciación para los elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="f68ee-105">Defines the child elements and sequencing information for calendar elements.</span></span>

``` syntax
<xs:complexType name="calendarTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:choice>
                    <xs:element name="ScheduleByDay"
                        type="dailyScheduleType"
                     />
                    <xs:element name="ScheduleByWeek"
                        type="weeklyScheduleType"
                     />
                    <xs:element name="ScheduleByMonth"
                        type="monthlyScheduleType"
                     />
                    <xs:element name="ScheduleByMonthDayOfWeek"
                        type="monthlyDayOfWeekScheduleType"
                     />
                </xs:choice>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f68ee-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f68ee-106">Child elements</span></span>



| <span data-ttu-id="f68ee-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f68ee-107">Element</span></span>                                                                                                      | <span data-ttu-id="f68ee-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f68ee-108">Type</span></span>                                                                                                 | <span data-ttu-id="f68ee-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f68ee-109">Description</span></span>                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f68ee-110">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="f68ee-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | <span data-ttu-id="f68ee-111">duration</span><span class="sxs-lookup"><span data-stu-id="f68ee-111">duration</span></span>                                                                                             | <span data-ttu-id="f68ee-112">Contiene el tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="f68ee-112">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="f68ee-113">El formato de esta cadena es P <days> DT <hours> H <minutes> M <seconds> S (por ejemplo, P2DT5S es un retraso de 2 días y 5 segundos).</span><span class="sxs-lookup"><span data-stu-id="f68ee-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, P2DT5S is a 2 day, 5 second delay).</span></span><br/> |
| [<span data-ttu-id="f68ee-114">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="f68ee-114">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [<span data-ttu-id="f68ee-115">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="f68ee-115">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)                       | <span data-ttu-id="f68ee-116">Especifica una programación diaria.</span><span class="sxs-lookup"><span data-stu-id="f68ee-116">Specifies a daily schedule.</span></span> <span data-ttu-id="f68ee-117">Por ejemplo, la tarea se inicia cada día, cada día, cada tres días, etc.</span><span class="sxs-lookup"><span data-stu-id="f68ee-117">For example, the task starts every day, every-other day, every third day, and so on.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="f68ee-118">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="f68ee-118">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [<span data-ttu-id="f68ee-119">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="f68ee-119">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)                   | <span data-ttu-id="f68ee-120">Especifica una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="f68ee-120">Specifies a monthly schedule.</span></span> <span data-ttu-id="f68ee-121">Por ejemplo, la tarea comienza a las 8:00 AM en días específicos del mes en meses específicos.</span><span class="sxs-lookup"><span data-stu-id="f68ee-121">For example, the task starts at 8:00 AM on specific days of the month on specific months.</span></span> <br/>                                                                                                       |
| [<span data-ttu-id="f68ee-122">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="f68ee-122">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="f68ee-123">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="f68ee-123">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="f68ee-124">Especifica un desencadenador que inicia un trabajo en una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="f68ee-124">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span> <span data-ttu-id="f68ee-125">Por ejemplo, la tarea se inicia en determinados días de la semana, semanas del mes y meses del año.</span><span class="sxs-lookup"><span data-stu-id="f68ee-125">For example, the task starts on specific days of the week, weeks of the month, and months of the year.</span></span> <br/>                                               |
| [<span data-ttu-id="f68ee-126">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="f68ee-126">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [<span data-ttu-id="f68ee-127">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="f68ee-127">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)                     | <span data-ttu-id="f68ee-128">Especifica una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="f68ee-128">Specifies a weekly schedule.</span></span> <span data-ttu-id="f68ee-129">Por ejemplo, la tarea comienza a las 8:00 A.M. en un día concreto de la semana cada semana o en un día concreto de la semana, cada dos semanas.</span><span class="sxs-lookup"><span data-stu-id="f68ee-129">For example, the task starts at 8:00 AM on a specific day of the week every week or on a specific day of the week every other week.</span></span> <br/>                                                              |



## <a name="remarks"></a><span data-ttu-id="f68ee-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f68ee-130">Remarks</span></span>

<span data-ttu-id="f68ee-131">Además del elemento secundario que se define aquí, el elemento [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) también utiliza los elementos secundarios definidos por el tipo complejo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f68ee-131">In addition to the child element defined here, the [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) element also uses the child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="f68ee-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f68ee-132">Requirements</span></span>



| <span data-ttu-id="f68ee-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f68ee-133">Requirement</span></span> | <span data-ttu-id="f68ee-134">Value</span><span class="sxs-lookup"><span data-stu-id="f68ee-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f68ee-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f68ee-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f68ee-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f68ee-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f68ee-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f68ee-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f68ee-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f68ee-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f68ee-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="f68ee-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f68ee-140">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f68ee-140">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="f68ee-141">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f68ee-141">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





