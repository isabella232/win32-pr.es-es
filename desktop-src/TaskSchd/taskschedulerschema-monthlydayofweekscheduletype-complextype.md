---
title: Tipo complejo de monthlyDayOfWeekScheduleType
description: Define los elementos secundarios y la información de secuenciación para el elemento ScheduleByMonthDayOfWeek.
ms.assetid: fb4e5ba3-592b-47a4-bedf-5181d2b7a50f
keywords:
- tipo complejo de monthlyDayOfWeekScheduleType Programador de tareas
topic_type:
- apiref
api_name:
- monthlyDayOfWeekScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 782715aed5cbf59a98e996bfa18fdd7c1022227a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676878"
---
# <a name="monthlydayofweekscheduletype-complex-type"></a><span data-ttu-id="ff200-104">Tipo complejo de monthlyDayOfWeekScheduleType</span><span class="sxs-lookup"><span data-stu-id="ff200-104">monthlyDayOfWeekScheduleType Complex Type</span></span>

<span data-ttu-id="ff200-105">Define los elementos secundarios y la información de secuenciación para el elemento [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ff200-105">Defines the child elements and sequencing information for the [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="monthlyDayOfWeekScheduleType">
    <xs:all>
        <xs:element name="Weeks"
            type="weeksType"
            minOccurs="0"
         />
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ff200-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ff200-106">Child elements</span></span>



| <span data-ttu-id="ff200-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="ff200-107">Element</span></span>                                                                                   | <span data-ttu-id="ff200-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff200-108">Type</span></span>                                                                     | <span data-ttu-id="ff200-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff200-109">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="ff200-110">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="ff200-110">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="ff200-111">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="ff200-111">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="ff200-112">Especifica los días de la semana durante los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="ff200-112">Specifies the days of the week during which the task runs.</span></span><br/>   |
| [<span data-ttu-id="ff200-113">**Partir**</span><span class="sxs-lookup"><span data-stu-id="ff200-113">**Months**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [<span data-ttu-id="ff200-114">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="ff200-114">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)         | <span data-ttu-id="ff200-115">Especifica los meses del año en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="ff200-115">Specifies the months of the year during which the task runs.</span></span><br/> |
| [<span data-ttu-id="ff200-116">**Semanas**</span><span class="sxs-lookup"><span data-stu-id="ff200-116">**Weeks**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | [<span data-ttu-id="ff200-117">**weeksType**</span><span class="sxs-lookup"><span data-stu-id="ff200-117">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md)           | <span data-ttu-id="ff200-118">Especifica las semanas del mes en las que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="ff200-118">Specifies the weeks of the month during which the task runs.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ff200-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff200-119">Requirements</span></span>



| <span data-ttu-id="ff200-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff200-120">Requirement</span></span> | <span data-ttu-id="ff200-121">Value</span><span class="sxs-lookup"><span data-stu-id="ff200-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff200-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff200-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ff200-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ff200-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ff200-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff200-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ff200-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff200-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff200-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff200-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff200-127">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ff200-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="ff200-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ff200-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





