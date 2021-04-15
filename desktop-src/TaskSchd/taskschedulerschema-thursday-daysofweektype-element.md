---
title: Elemento jueves (daysOfWeekType)
description: Especifica que la tarea se ejecuta el jueves.
ms.assetid: 01d0e7e8-7135-4f43-9d8f-b50c002b93bc
keywords:
- Programador de tareas del elemento jueves
topic_type:
- apiref
api_name:
- Thursday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12b1fb602411a9e4562a044b044e43de4800f239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676869"
---
# <a name="thursday-daysofweektype-element"></a><span data-ttu-id="624b1-104">Elemento jueves (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="624b1-104">Thursday (daysOfWeekType) Element</span></span>

<span data-ttu-id="624b1-105">Especifica que la tarea se ejecuta el jueves.</span><span class="sxs-lookup"><span data-stu-id="624b1-105">Specifies that the task runs on Thursday.</span></span>

``` syntax
<xs:element name="Thursday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="624b1-106">El elemento **jueves** se define mediante el tipo complejo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="624b1-106">The **Thursday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="624b1-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="624b1-107">Parent element</span></span>



| <span data-ttu-id="624b1-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="624b1-108">Element</span></span>                                                                                                                  | <span data-ttu-id="624b1-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="624b1-109">Derived from</span></span>                                                             | <span data-ttu-id="624b1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="624b1-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="624b1-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="624b1-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="624b1-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="624b1-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="624b1-113">Especifica los días de la semana en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="624b1-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="624b1-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="624b1-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="624b1-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="624b1-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="624b1-116">Especifica los días de la semana en los que se ejecuta la tarea para una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="624b1-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="624b1-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="624b1-117">Examples</span></span>

<span data-ttu-id="624b1-118">El siguiente código XML define un calendario de día de la semana que inicia una tarea el jueves.</span><span class="sxs-lookup"><span data-stu-id="624b1-118">The following XML defines a day of week calendar that starts a task on Thursday.</span></span>


```XML
<DaysOfWeek>
    <Thursday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="624b1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="624b1-119">Requirements</span></span>



| <span data-ttu-id="624b1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="624b1-120">Requirement</span></span> | <span data-ttu-id="624b1-121">Value</span><span class="sxs-lookup"><span data-stu-id="624b1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="624b1-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="624b1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="624b1-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="624b1-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="624b1-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="624b1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="624b1-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="624b1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="624b1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="624b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="624b1-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="624b1-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="624b1-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="624b1-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





