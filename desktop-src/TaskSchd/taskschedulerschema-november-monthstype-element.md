---
title: Elemento de noviembre (monthsType)
description: Especifica que la tarea se ejecuta en noviembre.
ms.assetid: 45f8c47b-3884-4f18-8275-f29f82ee32e2
keywords:
- Programador de tareas del elemento de noviembre
topic_type:
- apiref
api_name:
- November
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 295b63a4ff4dad1ec07504bb43c4a471d4389159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686040"
---
# <a name="november-monthstype-element"></a><span data-ttu-id="41c65-104">Elemento de noviembre (monthsType)</span><span class="sxs-lookup"><span data-stu-id="41c65-104">November (monthsType) Element</span></span>

<span data-ttu-id="41c65-105">Especifica que la tarea se ejecuta en noviembre.</span><span class="sxs-lookup"><span data-stu-id="41c65-105">Specifies that the task runs in November.</span></span>

``` syntax
<xs:element name="November">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="41c65-106">El elemento de **noviembre** se define mediante el tipo complejo de [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="41c65-106">The **November** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="41c65-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="41c65-107">Parent element</span></span>



| <span data-ttu-id="41c65-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="41c65-108">Element</span></span>                                                                                                          | <span data-ttu-id="41c65-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="41c65-109">Derived from</span></span>                                                     | <span data-ttu-id="41c65-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="41c65-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41c65-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="41c65-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="41c65-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="41c65-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="41c65-113">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="41c65-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="41c65-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="41c65-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="41c65-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="41c65-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="41c65-116">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="41c65-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="41c65-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="41c65-117">Examples</span></span>

<span data-ttu-id="41c65-118">El siguiente código XML define un calendario de meses que ejecuta la tarea en noviembre.</span><span class="sxs-lookup"><span data-stu-id="41c65-118">The following XML defines a months calendar that runs the task in November.</span></span>


```XML
<Months>
    <November/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="41c65-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41c65-119">Requirements</span></span>



| <span data-ttu-id="41c65-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="41c65-120">Requirement</span></span> | <span data-ttu-id="41c65-121">Value</span><span class="sxs-lookup"><span data-stu-id="41c65-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="41c65-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41c65-122">Minimum supported client</span></span><br/> | <span data-ttu-id="41c65-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="41c65-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="41c65-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41c65-124">Minimum supported server</span></span><br/> | <span data-ttu-id="41c65-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="41c65-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41c65-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="41c65-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c65-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="41c65-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="41c65-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="41c65-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





