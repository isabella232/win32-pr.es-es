---
title: Elemento de enero (monthsType)
description: Especifica que la tarea se ejecuta en enero.
ms.assetid: 3a0dde08-f2de-4ff4-9c5a-4368ff7a0e2c
keywords:
- Programador de tareas del elemento de enero
topic_type:
- apiref
api_name:
- January
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e72967f0fb6addb70af1792ffabf0457b1d20c29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801483"
---
# <a name="january-monthstype-element"></a><span data-ttu-id="6faff-104">Elemento de enero (monthsType)</span><span class="sxs-lookup"><span data-stu-id="6faff-104">January (monthsType) Element</span></span>

<span data-ttu-id="6faff-105">Especifica que la tarea se ejecuta en enero.</span><span class="sxs-lookup"><span data-stu-id="6faff-105">Specifies that the task runs in January.</span></span>

``` syntax
<xs:element name="January">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="6faff-106">El elemento de **enero** se define mediante el tipo complejo de [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6faff-106">The **January** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6faff-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="6faff-107">Parent element</span></span>



| <span data-ttu-id="6faff-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6faff-108">Element</span></span>                                                                                                          | <span data-ttu-id="6faff-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="6faff-109">Derived from</span></span>                                                     | <span data-ttu-id="6faff-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6faff-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6faff-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="6faff-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="6faff-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="6faff-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="6faff-113">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="6faff-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="6faff-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="6faff-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="6faff-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="6faff-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="6faff-116">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="6faff-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="6faff-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6faff-117">Examples</span></span>

<span data-ttu-id="6faff-118">El siguiente código XML define un calendario de meses que ejecuta la tarea en enero.</span><span class="sxs-lookup"><span data-stu-id="6faff-118">The following XML defines a months calendar that runs the task in January.</span></span>


```XML
<Months>
    <January/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="6faff-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6faff-119">Requirements</span></span>



| <span data-ttu-id="6faff-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6faff-120">Requirement</span></span> | <span data-ttu-id="6faff-121">Value</span><span class="sxs-lookup"><span data-stu-id="6faff-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6faff-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6faff-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6faff-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6faff-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6faff-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6faff-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6faff-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6faff-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6faff-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6faff-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6faff-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="6faff-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="6faff-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6faff-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





