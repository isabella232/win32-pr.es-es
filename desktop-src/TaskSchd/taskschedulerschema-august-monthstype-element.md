---
title: Elemento de agosto (monthsType)
description: Especifica que la tarea se ejecuta en agosto.
ms.assetid: cd7e528c-d482-4bb4-a31f-fccdb19a441b
keywords:
- Programador de tareas del elemento de agosto
topic_type:
- apiref
api_name:
- August
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4978ebd8f22da6e157461791c4c2000fce9db6ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905386"
---
# <a name="august-monthstype-element"></a><span data-ttu-id="ee25e-104">Elemento de agosto (monthsType)</span><span class="sxs-lookup"><span data-stu-id="ee25e-104">August (monthsType) Element</span></span>

<span data-ttu-id="ee25e-105">Especifica que la tarea se ejecuta en agosto.</span><span class="sxs-lookup"><span data-stu-id="ee25e-105">Specifies that the task runs in August.</span></span>

``` syntax
<xs:element name="August">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="ee25e-106">El elemento de **agosto** se define mediante el tipo complejo de [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ee25e-106">The **August** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ee25e-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="ee25e-107">Parent element</span></span>



| <span data-ttu-id="ee25e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ee25e-108">Element</span></span>                                                                                                          | <span data-ttu-id="ee25e-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="ee25e-109">Derived from</span></span>                                                     | <span data-ttu-id="ee25e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee25e-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee25e-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="ee25e-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="ee25e-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="ee25e-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="ee25e-113">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ee25e-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="ee25e-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="ee25e-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="ee25e-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="ee25e-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="ee25e-116">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="ee25e-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="ee25e-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ee25e-117">Examples</span></span>

<span data-ttu-id="ee25e-118">El siguiente código XML define un calendario de meses que ejecuta la tarea en agosto.</span><span class="sxs-lookup"><span data-stu-id="ee25e-118">The following XML defines a months calendar that runs the task in August.</span></span>


```XML
<Months>
    <August/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="ee25e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee25e-119">Requirements</span></span>



| <span data-ttu-id="ee25e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee25e-120">Requirement</span></span> | <span data-ttu-id="ee25e-121">Value</span><span class="sxs-lookup"><span data-stu-id="ee25e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ee25e-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee25e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ee25e-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ee25e-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ee25e-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee25e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ee25e-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ee25e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee25e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee25e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee25e-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="ee25e-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ee25e-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ee25e-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





