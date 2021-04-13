---
title: Tipo complejo de daysOfWeekType
description: Define los elementos secundarios y la información de secuenciación para los elementos DaysOfWeek (weeklyScheduleType) y DaysOfWeek (monthlyDayOfWeekScheduleType).
ms.assetid: b3315582-af7a-4d4c-8f6f-61de12a85f46
keywords:
- tipo complejo de daysOfWeekType Programador de tareas
topic_type:
- apiref
api_name:
- daysOfWeekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b4a1b5e6aeaa77c0bdfe12b1d5b68fde018f236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359865"
---
# <a name="daysofweektype-complex-type"></a><span data-ttu-id="5a2f5-104">Tipo complejo de daysOfWeekType</span><span class="sxs-lookup"><span data-stu-id="5a2f5-104">daysOfWeekType Complex Type</span></span>

<span data-ttu-id="5a2f5-105">Define los elementos secundarios y la información de secuenciación para los elementos [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) y [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5a2f5-105">Defines the child elements and sequencing information for the [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) and [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) elements.</span></span>

``` syntax
<xs:complexType name="daysOfWeekType">
    <xs:all>
        <xs:element name="Monday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Tuesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Wednesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Thursday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Friday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Saturday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Sunday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5a2f5-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5a2f5-106">Child elements</span></span>



| <span data-ttu-id="5a2f5-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="5a2f5-107">Element</span></span>                                                                   | <span data-ttu-id="5a2f5-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="5a2f5-108">Type</span></span> | <span data-ttu-id="5a2f5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a2f5-109">Description</span></span>                         |
|---------------------------------------------------------------------------|------|-------------------------------------|
| [<span data-ttu-id="5a2f5-110">**Día**</span><span class="sxs-lookup"><span data-stu-id="5a2f5-110">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       | <span data-ttu-id="5a2f5-111">N/D</span><span class="sxs-lookup"><span data-stu-id="5a2f5-111">N/A</span></span>  | <span data-ttu-id="5a2f5-112">La tarea se ejecuta el viernes.</span><span class="sxs-lookup"><span data-stu-id="5a2f5-112">Task runs on Friday.</span></span> <br/>    |
| [<span data-ttu-id="5a2f5-113">**Lunes**</span><span class="sxs-lookup"><span data-stu-id="5a2f5-113">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       | <span data-ttu-id="5a2f5-114">N/D</span><span class="sxs-lookup"><span data-stu-id="5a2f5-114">N/A</span></span>  | <span data-ttu-id="5a2f5-115">La tarea se ejecuta el lunes.</span><span class="sxs-lookup"><span data-stu-id="5a2f5-115">Task runs on Monday.</span></span><br/>     |
| [<span data-ttu-id="5a2f5-116">**Sábado**</span><span class="sxs-lookup"><span data-stu-id="5a2f5-116">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   | <span data-ttu-id="5a2f5-117">N/D</span><span class="sxs-lookup"><span data-stu-id="5a2f5-117">N/A</span></span>  | <span data-ttu-id="5a2f5-118">La tarea se ejecuta el sábado.</span><span class="sxs-lookup"><span data-stu-id="5a2f5-118">Task runs on Saturday.</span></span> <br/>  |
| [<span data-ttu-id="5a2f5-119">**Domingo**</span><span class="sxs-lookup"><span data-stu-id="5a2f5-119">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       | <span data-ttu-id="5a2f5-120">N/D</span><span class="sxs-lookup"><span data-stu-id="5a2f5-120">N/A</span></span>  | <span data-ttu-id="5a2f5-121">La tarea se ejecuta el domingo.</span><span class="sxs-lookup"><span data-stu-id="5a2f5-121">Task runs on Sunday.</span></span> <br/>    |
| [<span data-ttu-id="5a2f5-122">**Martes**</span><span class="sxs-lookup"><span data-stu-id="5a2f5-122">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   | <span data-ttu-id="5a2f5-123">N/D</span><span class="sxs-lookup"><span data-stu-id="5a2f5-123">N/A</span></span>  | <span data-ttu-id="5a2f5-124">La tarea se ejecuta el jueves</span><span class="sxs-lookup"><span data-stu-id="5a2f5-124">Task runs on Thursday</span></span> <br/>   |
| [<span data-ttu-id="5a2f5-125">**Jueves**</span><span class="sxs-lookup"><span data-stu-id="5a2f5-125">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     | <span data-ttu-id="5a2f5-126">N/D</span><span class="sxs-lookup"><span data-stu-id="5a2f5-126">N/A</span></span>  | <span data-ttu-id="5a2f5-127">La tarea se ejecuta el martes.</span><span class="sxs-lookup"><span data-stu-id="5a2f5-127">Task runs on Tuesday.</span></span> <br/>   |
| [<span data-ttu-id="5a2f5-128">**Lunes**</span><span class="sxs-lookup"><span data-stu-id="5a2f5-128">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) | <span data-ttu-id="5a2f5-129">N/D</span><span class="sxs-lookup"><span data-stu-id="5a2f5-129">N/A</span></span>  | <span data-ttu-id="5a2f5-130">La tarea se ejecuta el miércoles.</span><span class="sxs-lookup"><span data-stu-id="5a2f5-130">Task runs on Wednesday.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="5a2f5-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a2f5-131">Requirements</span></span>



| <span data-ttu-id="5a2f5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a2f5-132">Requirement</span></span> | <span data-ttu-id="5a2f5-133">Value</span><span class="sxs-lookup"><span data-stu-id="5a2f5-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5a2f5-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a2f5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5a2f5-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5a2f5-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5a2f5-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a2f5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5a2f5-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a2f5-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a2f5-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a2f5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a2f5-139">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="5a2f5-139">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="5a2f5-140">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="5a2f5-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





