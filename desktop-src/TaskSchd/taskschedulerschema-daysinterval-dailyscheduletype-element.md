---
title: Elemento DaysInterval (dailyScheduleType)
description: Especifica el intervalo entre los días de la programación.
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- Programador de tareas del elemento DaysInterval
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97b50581aa4825b31983a234a5eb47ff7b7b7e06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996035"
---
# <a name="daysinterval-dailyscheduletype-element"></a><span data-ttu-id="8fff0-104">Elemento DaysInterval (dailyScheduleType)</span><span class="sxs-lookup"><span data-stu-id="8fff0-104">DaysInterval (dailyScheduleType) Element</span></span>

<span data-ttu-id="8fff0-105">Especifica el intervalo entre los días de la programación.</span><span class="sxs-lookup"><span data-stu-id="8fff0-105">Specifies the interval between the days in the schedule.</span></span>

``` syntax
<xs:element name="DaysInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedInt"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="365"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="8fff0-106">El elemento se define mediante el tipo complejo de [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8fff0-106">The element is defined by the [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8fff0-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="8fff0-107">Parent element</span></span>



| <span data-ttu-id="8fff0-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="8fff0-108">Element</span></span>                                                                                | <span data-ttu-id="8fff0-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="8fff0-109">Derived from</span></span>                                                                   | <span data-ttu-id="8fff0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fff0-110">Description</span></span>                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="8fff0-111">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="8fff0-111">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [<span data-ttu-id="8fff0-112">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="8fff0-112">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md) | <span data-ttu-id="8fff0-113">Especifica una programación diaria.</span><span class="sxs-lookup"><span data-stu-id="8fff0-113">Specifies a daily schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8fff0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8fff0-114">Remarks</span></span>

<span data-ttu-id="8fff0-115">Para el desarrollo de scripts, el intervalo de días para un desencadenador diario se especifica mediante la propiedad [**DailyTrigger. DaysInterval**](dailytrigger-daysinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="8fff0-115">For script development, the days interval for a daily trigger is specified by the [**DailyTrigger.DaysInterval**](dailytrigger-daysinterval.md) property.</span></span>

<span data-ttu-id="8fff0-116">En el desarrollo de C++, el intervalo de días para un desencadenador diario se especifica mediante la propiedad [**IDailyTrigger::D aysinterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) .</span><span class="sxs-lookup"><span data-stu-id="8fff0-116">For C++ development, the days interval for a daily trigger is specified by the [**IDailyTrigger::DaysInterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="8fff0-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8fff0-117">Examples</span></span>

<span data-ttu-id="8fff0-118">En el código XML siguiente se define un desencadenador de calendario diario que inicia la tarea cada día.</span><span class="sxs-lookup"><span data-stu-id="8fff0-118">The following XML defines a daily calendar trigger that starts the task every day.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



<span data-ttu-id="8fff0-119">Para obtener un ejemplo completo del XML de una tarea que especifica una programación diaria, vea [ejemplo de desencadenador diario (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="8fff0-119">For a complete example of the XML for a task that specifies a daily schedule, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8fff0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fff0-120">Requirements</span></span>



| <span data-ttu-id="8fff0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fff0-121">Requirement</span></span> | <span data-ttu-id="8fff0-122">Value</span><span class="sxs-lookup"><span data-stu-id="8fff0-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8fff0-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fff0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8fff0-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8fff0-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8fff0-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fff0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8fff0-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8fff0-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8fff0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fff0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fff0-128">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="8fff0-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="8fff0-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="8fff0-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





