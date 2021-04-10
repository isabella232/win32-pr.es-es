---
title: Elemento Sunday (daysOfWeekType)
description: Especifica que la tarea se ejecuta el domingo.
ms.assetid: 856db869-2273-4bb8-88c8-c126bb16c87b
keywords:
- Sunday, elemento Programador de tareas
topic_type:
- apiref
api_name:
- Sunday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40efba31b392da5959853feeb1cae567cee25cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150843"
---
# <a name="sunday-daysofweektype-element"></a><span data-ttu-id="6fc93-104">Elemento Sunday (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="6fc93-104">Sunday (daysOfWeekType) Element</span></span>

<span data-ttu-id="6fc93-105">Especifica que la tarea se ejecuta el domingo.</span><span class="sxs-lookup"><span data-stu-id="6fc93-105">Specifies that the task runs on Sunday.</span></span>

``` syntax
<xs:element name="Sunday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="6fc93-106">El elemento **Sunday** se define mediante el tipo complejo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6fc93-106">The **Sunday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6fc93-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="6fc93-107">Parent element</span></span>



| <span data-ttu-id="6fc93-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6fc93-108">Element</span></span>                                                                                                                  | <span data-ttu-id="6fc93-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="6fc93-109">Derived from</span></span>                                                             | <span data-ttu-id="6fc93-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fc93-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6fc93-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="6fc93-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="6fc93-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="6fc93-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="6fc93-113">Especifica los días de la semana en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="6fc93-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="6fc93-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="6fc93-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="6fc93-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="6fc93-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="6fc93-116">Especifica los días de la semana en los que se ejecuta la tarea para una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="6fc93-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="6fc93-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6fc93-117">Examples</span></span>

<span data-ttu-id="6fc93-118">El siguiente código XML define un calendario de día de la semana que inicia una tarea el domingo.</span><span class="sxs-lookup"><span data-stu-id="6fc93-118">The following XML defines a day of week calendar that starts a task on Sunday.</span></span>


```XML
<DaysOfWeek>
    <Sunday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="6fc93-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fc93-119">Requirements</span></span>



| <span data-ttu-id="6fc93-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fc93-120">Requirement</span></span> | <span data-ttu-id="6fc93-121">Value</span><span class="sxs-lookup"><span data-stu-id="6fc93-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6fc93-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fc93-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6fc93-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6fc93-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6fc93-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fc93-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6fc93-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6fc93-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6fc93-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6fc93-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fc93-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="6fc93-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="6fc93-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6fc93-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





