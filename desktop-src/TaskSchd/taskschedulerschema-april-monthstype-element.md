---
title: Elemento April (monthsType)
description: Especifica que la tarea se ejecuta en abril.
ms.assetid: b642e142-0acc-4b88-a86a-5d539613ead6
keywords:
- April (elemento) Programador de tareas
topic_type:
- apiref
api_name:
- April
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecde82e5091adf51c2e42b682e36dba6d45e85c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151021"
---
# <a name="april-monthstype-element"></a><span data-ttu-id="aa823-104">Elemento April (monthsType)</span><span class="sxs-lookup"><span data-stu-id="aa823-104">April (monthsType) Element</span></span>

<span data-ttu-id="aa823-105">Especifica que la tarea se ejecuta en abril.</span><span class="sxs-lookup"><span data-stu-id="aa823-105">Specifies that the task runs in April.</span></span>

``` syntax
<xs:element name="April">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="aa823-106">El elemento **April** se define mediante el tipo complejo [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="aa823-106">The **April** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="aa823-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="aa823-107">Parent element</span></span>



| <span data-ttu-id="aa823-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="aa823-108">Element</span></span>                                                                                                          | <span data-ttu-id="aa823-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="aa823-109">Derived from</span></span>                                                     | <span data-ttu-id="aa823-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa823-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa823-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="aa823-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="aa823-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="aa823-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="aa823-113">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="aa823-113">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |
| [<span data-ttu-id="aa823-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="aa823-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="aa823-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="aa823-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="aa823-116">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="aa823-116">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="aa823-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="aa823-117">Examples</span></span>

<span data-ttu-id="aa823-118">El siguiente código XML define un calendario de meses que ejecuta la tarea en abril.</span><span class="sxs-lookup"><span data-stu-id="aa823-118">The following XML defines a months calendar that runs the task in April.</span></span>


```XML
<Months>
    <April/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="aa823-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa823-119">Requirements</span></span>



| <span data-ttu-id="aa823-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa823-120">Requirement</span></span> | <span data-ttu-id="aa823-121">Value</span><span class="sxs-lookup"><span data-stu-id="aa823-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa823-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa823-122">Minimum supported client</span></span><br/> | <span data-ttu-id="aa823-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="aa823-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aa823-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa823-124">Minimum supported server</span></span><br/> | <span data-ttu-id="aa823-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa823-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa823-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa823-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa823-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="aa823-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="aa823-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="aa823-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





