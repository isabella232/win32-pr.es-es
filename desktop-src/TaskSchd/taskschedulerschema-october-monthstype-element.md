---
title: Elemento de octubre (monthsType)
description: Especifica que la tarea se ejecuta en octubre.
ms.assetid: 62c8bb3e-a70f-45b8-8d80-7a7eef9dfaeb
keywords:
- Programador de tareas del elemento de octubre
topic_type:
- apiref
api_name:
- October
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79bf2a2dde46341f48808342ab6aefb78863524b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151179"
---
# <a name="october-monthstype-element"></a><span data-ttu-id="11736-104">Elemento de octubre (monthsType)</span><span class="sxs-lookup"><span data-stu-id="11736-104">October (monthsType) Element</span></span>

<span data-ttu-id="11736-105">Especifica que la tarea se ejecuta en octubre.</span><span class="sxs-lookup"><span data-stu-id="11736-105">Specifies that the task runs in October.</span></span>

``` syntax
<xs:element name="October">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="11736-106">El elemento de **octubre** se define mediante el tipo complejo de [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="11736-106">The **October** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="11736-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="11736-107">Parent element</span></span>



| <span data-ttu-id="11736-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="11736-108">Element</span></span>                                                                                                          | <span data-ttu-id="11736-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="11736-109">Derived from</span></span>                                                     | <span data-ttu-id="11736-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="11736-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11736-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="11736-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="11736-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="11736-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="11736-113">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="11736-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="11736-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="11736-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="11736-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="11736-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="11736-116">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="11736-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="11736-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="11736-117">Examples</span></span>

<span data-ttu-id="11736-118">El siguiente código XML define un calendario de meses que ejecuta la tarea en octubre.</span><span class="sxs-lookup"><span data-stu-id="11736-118">The following XML defines a months calendar that runs the task in October.</span></span>


```XML
<Months>
    <October/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="11736-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11736-119">Requirements</span></span>



| <span data-ttu-id="11736-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="11736-120">Requirement</span></span> | <span data-ttu-id="11736-121">Value</span><span class="sxs-lookup"><span data-stu-id="11736-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="11736-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11736-122">Minimum supported client</span></span><br/> | <span data-ttu-id="11736-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="11736-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="11736-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11736-124">Minimum supported server</span></span><br/> | <span data-ttu-id="11736-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="11736-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11736-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="11736-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11736-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="11736-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="11736-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="11736-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





