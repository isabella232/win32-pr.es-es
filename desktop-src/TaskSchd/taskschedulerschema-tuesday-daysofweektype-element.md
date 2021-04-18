---
title: Elemento Tuesday (daysOfWeekType)
description: Especifica que la tarea se ejecuta el martes.
ms.assetid: 588608e9-33f9-405d-8b4b-35f11ab403db
keywords:
- Tuesday (elemento) Programador de tareas
topic_type:
- apiref
api_name:
- Tuesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ed48803d0cad5dae409202869c600e7e7a60643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676991"
---
# <a name="tuesday-daysofweektype-element"></a><span data-ttu-id="e8db9-104">Elemento Tuesday (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="e8db9-104">Tuesday (daysOfWeekType) Element</span></span>

<span data-ttu-id="e8db9-105">Especifica que la tarea se ejecuta el martes.</span><span class="sxs-lookup"><span data-stu-id="e8db9-105">Specifies that the task runs on Tuesday.</span></span>

``` syntax
<xs:element name="Tuesday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="e8db9-106">El elemento **Tuesday** se define mediante el tipo complejo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e8db9-106">The **Tuesday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e8db9-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="e8db9-107">Parent element</span></span>



| <span data-ttu-id="e8db9-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e8db9-108">Element</span></span>                                                                                                                  | <span data-ttu-id="e8db9-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e8db9-109">Derived from</span></span>                                                             | <span data-ttu-id="e8db9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8db9-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8db9-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="e8db9-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="e8db9-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="e8db9-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="e8db9-113">Especifica los días de la semana en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="e8db9-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="e8db9-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="e8db9-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="e8db9-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="e8db9-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="e8db9-116">Especifica los días de la semana en los que se ejecuta la tarea para una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="e8db9-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="e8db9-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e8db9-117">Examples</span></span>

<span data-ttu-id="e8db9-118">El siguiente código XML define un calendario de día de la semana que inicia una tarea el martes.</span><span class="sxs-lookup"><span data-stu-id="e8db9-118">The following XML defines a day of week calendar that starts a task on Tuesday.</span></span>


```XML
<DaysOfWeek>
    <Tuesday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="e8db9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8db9-119">Requirements</span></span>



| <span data-ttu-id="e8db9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8db9-120">Requirement</span></span> | <span data-ttu-id="e8db9-121">Value</span><span class="sxs-lookup"><span data-stu-id="e8db9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e8db9-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8db9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e8db9-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e8db9-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e8db9-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8db9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e8db9-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8db9-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8db9-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8db9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8db9-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="e8db9-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e8db9-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="e8db9-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





