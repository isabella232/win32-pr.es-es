---
title: Elemento May (monthsType)
description: Especifica que la tarea se ejecuta en mayo.
ms.assetid: 1fcc3eb7-6500-4ba3-b146-14d169d9b445
keywords:
- Elemento puede Programador de tareas
topic_type:
- apiref
api_name:
- May
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d3f0c107124aa2c87672f63a469857f3795e13c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676871"
---
# <a name="may-monthstype-element"></a><span data-ttu-id="f99c8-104">Elemento May (monthsType)</span><span class="sxs-lookup"><span data-stu-id="f99c8-104">May (monthsType) Element</span></span>

<span data-ttu-id="f99c8-105">Especifica que la tarea se ejecuta en mayo.</span><span class="sxs-lookup"><span data-stu-id="f99c8-105">Specifies that the task runs in May.</span></span>

``` syntax
<xs:element name="May">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="f99c8-106">El elemento **puede estar** definido por el tipo complejo [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f99c8-106">The **May** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f99c8-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="f99c8-107">Parent element</span></span>



| <span data-ttu-id="f99c8-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f99c8-108">Element</span></span>                                                                                                          | <span data-ttu-id="f99c8-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f99c8-109">Derived from</span></span>                                                     | <span data-ttu-id="f99c8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f99c8-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f99c8-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="f99c8-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="f99c8-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="f99c8-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="f99c8-113">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="f99c8-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="f99c8-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="f99c8-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="f99c8-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="f99c8-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="f99c8-116">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="f99c8-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="f99c8-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f99c8-117">Examples</span></span>

<span data-ttu-id="f99c8-118">En el código XML siguiente se define un calendario de meses que ejecuta la tarea en mayo.</span><span class="sxs-lookup"><span data-stu-id="f99c8-118">The following XML defines a months calendar that runs the task in May.</span></span>


```XML
<Months>
    <May/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="f99c8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f99c8-119">Requirements</span></span>



| <span data-ttu-id="f99c8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f99c8-120">Requirement</span></span> | <span data-ttu-id="f99c8-121">Value</span><span class="sxs-lookup"><span data-stu-id="f99c8-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f99c8-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f99c8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f99c8-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f99c8-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f99c8-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f99c8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f99c8-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f99c8-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f99c8-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f99c8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f99c8-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="f99c8-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f99c8-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f99c8-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





