---
title: Elemento de febrero (monthsType)
description: Especifica que la tarea se ejecuta en febrero.
ms.assetid: 871449f8-fa3a-4e1f-be36-bc5c98125721
keywords:
- Elemento de febrero Programador de tareas
topic_type:
- apiref
api_name:
- February
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 727751964bfb9a752eb1190f8c7d3a86de2a9413
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676941"
---
# <a name="february-monthstype-element"></a><span data-ttu-id="c3154-104">Elemento de febrero (monthsType)</span><span class="sxs-lookup"><span data-stu-id="c3154-104">February (monthsType) Element</span></span>

<span data-ttu-id="c3154-105">Especifica que la tarea se ejecuta en febrero.</span><span class="sxs-lookup"><span data-stu-id="c3154-105">Specifies that the task runs in February.</span></span>

``` syntax
<xs:element name="February">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="c3154-106">El elemento de **febrero** se define mediante el tipo complejo de [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c3154-106">The **February** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c3154-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="c3154-107">Parent element</span></span>



| <span data-ttu-id="c3154-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c3154-108">Element</span></span>                                                                                                          | <span data-ttu-id="c3154-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="c3154-109">Derived from</span></span>                                                     | <span data-ttu-id="c3154-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3154-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3154-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c3154-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="c3154-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="c3154-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="c3154-113">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="c3154-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="c3154-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c3154-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="c3154-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="c3154-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="c3154-116">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="c3154-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="c3154-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c3154-117">Examples</span></span>

<span data-ttu-id="c3154-118">El siguiente código XML define un calendario de meses que ejecuta la tarea en febrero.</span><span class="sxs-lookup"><span data-stu-id="c3154-118">The following XML defines a months calendar that runs the task in February.</span></span>


```XML
<Months>
    <February/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="c3154-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3154-119">Requirements</span></span>



| <span data-ttu-id="c3154-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3154-120">Requirement</span></span> | <span data-ttu-id="c3154-121">Value</span><span class="sxs-lookup"><span data-stu-id="c3154-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c3154-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3154-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c3154-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c3154-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c3154-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3154-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c3154-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c3154-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3154-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3154-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3154-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="c3154-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c3154-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="c3154-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





