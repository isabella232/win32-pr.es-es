---
title: Sábado (daysOfWeekType) (elemento)
description: Especifica que la tarea se ejecuta el sábado.
ms.assetid: def26a72-c143-466a-b5b0-6105078afffa
keywords:
- Sábado Programador de tareas del elemento
topic_type:
- apiref
api_name:
- Saturday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b5f7cb36002b2add64cdea541caa2fd28df37ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803320"
---
# <a name="saturday-daysofweektype-element"></a><span data-ttu-id="0ec8a-104">Sábado (daysOfWeekType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="0ec8a-104">Saturday (daysOfWeekType) Element</span></span>

<span data-ttu-id="0ec8a-105">Especifica que la tarea se ejecuta el sábado.</span><span class="sxs-lookup"><span data-stu-id="0ec8a-105">Specifies that the task runs on Saturday.</span></span>

``` syntax
<xs:element name="Saturday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="0ec8a-106">El elemento **sábado** se define mediante el tipo complejo de [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0ec8a-106">The **Saturday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0ec8a-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="0ec8a-107">Parent element</span></span>



| <span data-ttu-id="0ec8a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="0ec8a-108">Element</span></span>                                                                                                                  | <span data-ttu-id="0ec8a-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="0ec8a-109">Derived from</span></span>                                                             | <span data-ttu-id="0ec8a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ec8a-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ec8a-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="0ec8a-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="0ec8a-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="0ec8a-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="0ec8a-113">Especifica los días de la semana en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="0ec8a-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="0ec8a-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="0ec8a-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="0ec8a-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="0ec8a-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="0ec8a-116">Especifica los días de la semana en los que se ejecuta la tarea para una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="0ec8a-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="0ec8a-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0ec8a-117">Examples</span></span>

<span data-ttu-id="0ec8a-118">El siguiente código XML define un calendario de día de la semana que inicia una tarea el sábado.</span><span class="sxs-lookup"><span data-stu-id="0ec8a-118">The following XML defines a day of week calendar that starts a task on Saturday.</span></span>


```XML
<DaysOfWeek>
    <Saturday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="0ec8a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ec8a-119">Requirements</span></span>



| <span data-ttu-id="0ec8a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ec8a-120">Requirement</span></span> | <span data-ttu-id="0ec8a-121">Value</span><span class="sxs-lookup"><span data-stu-id="0ec8a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0ec8a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ec8a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0ec8a-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0ec8a-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0ec8a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ec8a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0ec8a-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ec8a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ec8a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ec8a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ec8a-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="0ec8a-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="0ec8a-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="0ec8a-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





