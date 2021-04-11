---
title: Friday (daysOfWeekType), elemento
description: Especifica que la tarea se ejecuta el viernes.
ms.assetid: bff85911-d354-4954-8c69-7b6f2ca312d3
keywords:
- Friday, elemento Programador de tareas
topic_type:
- apiref
api_name:
- Friday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 951142e7e925ea71ef1f833be4421351aaea3b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150800"
---
# <a name="friday-daysofweektype-element"></a><span data-ttu-id="c5351-104">Friday (daysOfWeekType), elemento</span><span class="sxs-lookup"><span data-stu-id="c5351-104">Friday (daysOfWeekType) Element</span></span>

<span data-ttu-id="c5351-105">Especifica que la tarea se ejecuta el viernes.</span><span class="sxs-lookup"><span data-stu-id="c5351-105">Specifies that the task runs on Friday.</span></span>

``` syntax
<xs:element name="Friday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="c5351-106">El elemento **Friday** se define mediante el tipo complejo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c5351-106">The **Friday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c5351-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="c5351-107">Parent element</span></span>



| <span data-ttu-id="c5351-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c5351-108">Element</span></span>                                                                                                                  | <span data-ttu-id="c5351-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="c5351-109">Derived from</span></span>                                                             | <span data-ttu-id="c5351-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5351-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5351-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c5351-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="c5351-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="c5351-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="c5351-113">Especifica los días de la semana en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="c5351-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="c5351-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c5351-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="c5351-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="c5351-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="c5351-116">Especifica los días de la semana en los que se ejecuta la tarea para una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="c5351-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="c5351-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c5351-117">Examples</span></span>

<span data-ttu-id="c5351-118">El siguiente código XML define un calendario de día de la semana que inicia una tarea el viernes.</span><span class="sxs-lookup"><span data-stu-id="c5351-118">The following XML defines a day of week calendar that starts a task on Friday.</span></span>


```XML
<DaysOfWeek>
    <Friday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="c5351-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5351-119">Requirements</span></span>



| <span data-ttu-id="c5351-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5351-120">Requirement</span></span> | <span data-ttu-id="c5351-121">Value</span><span class="sxs-lookup"><span data-stu-id="c5351-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c5351-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5351-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c5351-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c5351-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c5351-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5351-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c5351-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5351-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5351-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5351-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5351-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="c5351-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c5351-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="c5351-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





