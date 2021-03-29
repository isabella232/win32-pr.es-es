---
title: Lunes (daysOfWeekType) (elemento)
description: Especifica que la tarea se ejecuta el lunes.
ms.assetid: 2b7ce0c1-c635-47d0-b482-5c93c0028c92
keywords:
- Lunes Programador de tareas de elemento
topic_type:
- apiref
api_name:
- Monday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3967db32a6ccd536e2e389e84de4eec05b333634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492058"
---
# <a name="monday-daysofweektype-element"></a><span data-ttu-id="7a80e-104">Lunes (daysOfWeekType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="7a80e-104">Monday (daysOfWeekType) Element</span></span>

<span data-ttu-id="7a80e-105">Especifica que la tarea se ejecuta el lunes.</span><span class="sxs-lookup"><span data-stu-id="7a80e-105">Specifies that the task runs on Monday.</span></span>

``` syntax
<xs:element name="Monday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="7a80e-106">El elemento de **lunes** se define mediante el tipo complejo de [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7a80e-106">The **Monday** element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7a80e-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="7a80e-107">Parent element</span></span>



| <span data-ttu-id="7a80e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="7a80e-108">Element</span></span>                                                                                                                  | <span data-ttu-id="7a80e-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="7a80e-109">Derived from</span></span>                                                             | <span data-ttu-id="7a80e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a80e-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a80e-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="7a80e-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="7a80e-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="7a80e-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="7a80e-113">Especifica los días de la semana en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="7a80e-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="7a80e-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="7a80e-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="7a80e-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="7a80e-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="7a80e-116">Especifica los días de la semana en los que se ejecuta la tarea para una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="7a80e-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="7a80e-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7a80e-117">Examples</span></span>

<span data-ttu-id="7a80e-118">El siguiente código XML define un calendario de día de la semana que inicia una tarea el lunes.</span><span class="sxs-lookup"><span data-stu-id="7a80e-118">The following XML defines a day of week calendar that starts a task on Monday.</span></span>


```XML
<DaysOfWeek>
    <Monday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="7a80e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a80e-119">Requirements</span></span>



| <span data-ttu-id="7a80e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a80e-120">Requirement</span></span> | <span data-ttu-id="7a80e-121">Value</span><span class="sxs-lookup"><span data-stu-id="7a80e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7a80e-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a80e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7a80e-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7a80e-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7a80e-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a80e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7a80e-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7a80e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a80e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a80e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a80e-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="7a80e-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="7a80e-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="7a80e-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





