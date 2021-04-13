---
title: Elemento miércoles (daysOfWeekType)
description: Especifica que la tarea se ejecuta el miércoles.
ms.assetid: 6d4f52e2-4390-4f9d-bab8-813bd0851582
keywords:
- Miércoles, elemento Programador de tareas
topic_type:
- apiref
api_name:
- Wednesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f9d8c60cb7cea818cc0b096e99e97e8f1490d47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534869"
---
# <a name="wednesday-daysofweektype-element"></a><span data-ttu-id="39415-104">Elemento miércoles (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="39415-104">Wednesday (daysOfWeekType) Element</span></span>

<span data-ttu-id="39415-105">Especifica que la tarea se ejecuta el miércoles.</span><span class="sxs-lookup"><span data-stu-id="39415-105">Specifies that the task runs on Wednesday.</span></span>

``` syntax
<xs:element name="Wednesday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="39415-106">El elemento **miércoles** se define mediante el tipo complejo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="39415-106">The **Wednesday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="39415-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="39415-107">Parent element</span></span>



| <span data-ttu-id="39415-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="39415-108">Element</span></span>                                                                                                                  | <span data-ttu-id="39415-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="39415-109">Derived from</span></span>                                                             | <span data-ttu-id="39415-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="39415-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39415-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="39415-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="39415-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="39415-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="39415-113">Especifica los días de la semana en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="39415-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="39415-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="39415-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="39415-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="39415-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="39415-116">Especifica los días de la semana en los que se ejecuta la tarea para una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="39415-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="39415-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="39415-117">Examples</span></span>

<span data-ttu-id="39415-118">El siguiente código XML define un calendario de día de la semana que inicia una tarea el miércoles.</span><span class="sxs-lookup"><span data-stu-id="39415-118">The following XML defines a day of week calendar that starts a task on Wednesday.</span></span>


```XML
<DaysOfWeek>
    <Wednesday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="39415-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39415-119">Requirements</span></span>



| <span data-ttu-id="39415-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="39415-120">Requirement</span></span> | <span data-ttu-id="39415-121">Value</span><span class="sxs-lookup"><span data-stu-id="39415-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="39415-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39415-122">Minimum supported client</span></span><br/> | <span data-ttu-id="39415-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="39415-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="39415-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39415-124">Minimum supported server</span></span><br/> | <span data-ttu-id="39415-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="39415-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39415-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="39415-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39415-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="39415-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="39415-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="39415-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





