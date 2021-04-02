---
title: Elemento de septiembre (monthsType)
description: Especifica que la tarea se ejecuta en septiembre.
ms.assetid: b1ad2221-ca22-4808-bf20-ecf3cbb930f2
keywords:
- Programador de tareas del elemento de septiembre
topic_type:
- apiref
api_name:
- September
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdd7e18ba9ae1cc7653589710fb9529281e84ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996994"
---
# <a name="september-monthstype-element"></a><span data-ttu-id="ff7c0-104">Elemento de septiembre (monthsType)</span><span class="sxs-lookup"><span data-stu-id="ff7c0-104">September (monthsType) Element</span></span>

<span data-ttu-id="ff7c0-105">Especifica que la tarea se ejecuta en septiembre.</span><span class="sxs-lookup"><span data-stu-id="ff7c0-105">Specifies that the task runs in September.</span></span>

``` syntax
<xs:element name="September">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="ff7c0-106">El elemento de **septiembre** se define mediante el tipo complejo de [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ff7c0-106">The **September** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ff7c0-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="ff7c0-107">Parent element</span></span>



| <span data-ttu-id="ff7c0-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ff7c0-108">Element</span></span>                                                                                                          | <span data-ttu-id="ff7c0-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="ff7c0-109">Derived from</span></span>                                                     | <span data-ttu-id="ff7c0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff7c0-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff7c0-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="ff7c0-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="ff7c0-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="ff7c0-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="ff7c0-113">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ff7c0-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="ff7c0-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="ff7c0-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="ff7c0-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="ff7c0-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="ff7c0-116">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="ff7c0-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="ff7c0-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ff7c0-117">Examples</span></span>

<span data-ttu-id="ff7c0-118">El siguiente código XML define un calendario de meses que ejecuta la tarea en septiembre.</span><span class="sxs-lookup"><span data-stu-id="ff7c0-118">The following XML defines a months calendar that runs the task in September.</span></span>


```XML
<Months>
    <September/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="ff7c0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff7c0-119">Requirements</span></span>



| <span data-ttu-id="ff7c0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff7c0-120">Requirement</span></span> | <span data-ttu-id="ff7c0-121">Value</span><span class="sxs-lookup"><span data-stu-id="ff7c0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff7c0-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff7c0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ff7c0-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ff7c0-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ff7c0-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff7c0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ff7c0-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff7c0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff7c0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff7c0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff7c0-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="ff7c0-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ff7c0-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ff7c0-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





