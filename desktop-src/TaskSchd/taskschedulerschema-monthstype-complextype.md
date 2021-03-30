---
title: Tipo complejo de monthsType
description: Define los elementos secundarios e información de secuenciación para los elementos months (monthlyDayOfWeekScheduleType) y months (monthlyScheduleType).
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- tipo complejo de monthsType Programador de tareas
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6a19000073fd12e05aa915921850264979a0541
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801478"
---
# <a name="monthstype-complex-type"></a><span data-ttu-id="073b0-104">Tipo complejo de monthsType</span><span class="sxs-lookup"><span data-stu-id="073b0-104">monthsType Complex Type</span></span>

<span data-ttu-id="073b0-105">Define los elementos secundarios e información de secuenciación para los elementos [**months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) y [**months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="073b0-105">Defines the child elements and sequencing information for the [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) and [**Months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) elements.</span></span>

``` syntax
<xs:complexType name="monthsType">
    <xs:all>
        <xs:element name="January"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="February"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="March"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="April"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="May"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="June"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="July"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="August"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="September"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="October"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="November"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="December"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="073b0-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="073b0-106">Child elements</span></span>



| <span data-ttu-id="073b0-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="073b0-107">Element</span></span>                                                               | <span data-ttu-id="073b0-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="073b0-108">Type</span></span> | <span data-ttu-id="073b0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="073b0-109">Description</span></span>                                            |
|-----------------------------------------------------------------------|------|--------------------------------------------------------|
| [<span data-ttu-id="073b0-110">**April**</span><span class="sxs-lookup"><span data-stu-id="073b0-110">**April**</span></span>](taskschedulerschema-april-monthstype-element.md)         | <span data-ttu-id="073b0-111">N/D</span><span class="sxs-lookup"><span data-stu-id="073b0-111">N/A</span></span>  | <span data-ttu-id="073b0-112">Especifica que la tarea se ejecuta en abril.</span><span class="sxs-lookup"><span data-stu-id="073b0-112">Specifies that the task runs in April.</span></span> <br/>     |
| [<span data-ttu-id="073b0-113">**Agosto**</span><span class="sxs-lookup"><span data-stu-id="073b0-113">**August**</span></span>](taskschedulerschema-august-monthstype-element.md)       | <span data-ttu-id="073b0-114">N/D</span><span class="sxs-lookup"><span data-stu-id="073b0-114">N/A</span></span>  | <span data-ttu-id="073b0-115">Especifica que la tarea se ejecuta en agosto.</span><span class="sxs-lookup"><span data-stu-id="073b0-115">Specifies that the task runs in August.</span></span> <br/>    |
| [<span data-ttu-id="073b0-116">**Diciembre**</span><span class="sxs-lookup"><span data-stu-id="073b0-116">**December**</span></span>](taskschedulerschema-december-monthstype-element.md)   | <span data-ttu-id="073b0-117">N/D</span><span class="sxs-lookup"><span data-stu-id="073b0-117">N/A</span></span>  | <span data-ttu-id="073b0-118">Especifica que la tarea se ejecuta en diciembre.</span><span class="sxs-lookup"><span data-stu-id="073b0-118">Specifies that the task runs in December.</span></span> <br/>  |
| [<span data-ttu-id="073b0-119">**February**</span><span class="sxs-lookup"><span data-stu-id="073b0-119">**February**</span></span>](taskschedulerschema-february-monthstype-element.md)   | <span data-ttu-id="073b0-120">N/D</span><span class="sxs-lookup"><span data-stu-id="073b0-120">N/A</span></span>  | <span data-ttu-id="073b0-121">Especifica que la tarea se ejecuta en febrero.</span><span class="sxs-lookup"><span data-stu-id="073b0-121">Specifies that the task runs in February.</span></span> <br/>  |
| [<span data-ttu-id="073b0-122">**January**</span><span class="sxs-lookup"><span data-stu-id="073b0-122">**January**</span></span>](taskschedulerschema-january-monthstype-element.md)     | <span data-ttu-id="073b0-123">N/D</span><span class="sxs-lookup"><span data-stu-id="073b0-123">N/A</span></span>  | <span data-ttu-id="073b0-124">Especifica que la tarea se ejecuta en enero.</span><span class="sxs-lookup"><span data-stu-id="073b0-124">Specifies that the task runs in January.</span></span> <br/>   |
| [<span data-ttu-id="073b0-125">**Julio**</span><span class="sxs-lookup"><span data-stu-id="073b0-125">**July**</span></span>](taskschedulerschema-july-monthstype-element.md)           | <span data-ttu-id="073b0-126">N/D</span><span class="sxs-lookup"><span data-stu-id="073b0-126">N/A</span></span>  | <span data-ttu-id="073b0-127">Especifica que la tarea se ejecuta en julio.</span><span class="sxs-lookup"><span data-stu-id="073b0-127">Specifies that the task runs in July.</span></span> <br/>      |
| [<span data-ttu-id="073b0-128">**Junio**</span><span class="sxs-lookup"><span data-stu-id="073b0-128">**June**</span></span>](taskschedulerschema-june-monthstype-element.md)           | <span data-ttu-id="073b0-129">N/D</span><span class="sxs-lookup"><span data-stu-id="073b0-129">N/A</span></span>  | <span data-ttu-id="073b0-130">Especifica que la tarea se ejecuta en junio.</span><span class="sxs-lookup"><span data-stu-id="073b0-130">Specifies that the task runs in June.</span></span> <br/>      |
| [<span data-ttu-id="073b0-131">**Marzo**</span><span class="sxs-lookup"><span data-stu-id="073b0-131">**March**</span></span>](taskschedulerschema-march-monthstype-element.md)         | <span data-ttu-id="073b0-132">N/D</span><span class="sxs-lookup"><span data-stu-id="073b0-132">N/A</span></span>  | <span data-ttu-id="073b0-133">Especifica que la tarea se ejecuta en marzo.</span><span class="sxs-lookup"><span data-stu-id="073b0-133">Specifies that the task runs in March.</span></span> <br/>     |
| [<span data-ttu-id="073b0-134">**May**</span><span class="sxs-lookup"><span data-stu-id="073b0-134">**May**</span></span>](taskschedulerschema-may-monthstype-element.md)             | <span data-ttu-id="073b0-135">N/D</span><span class="sxs-lookup"><span data-stu-id="073b0-135">N/A</span></span>  | <span data-ttu-id="073b0-136">Especifica que la tarea se ejecuta en mayo.</span><span class="sxs-lookup"><span data-stu-id="073b0-136">Specifies that the task runs in May.</span></span> <br/>       |
| [<span data-ttu-id="073b0-137">**Noviembre**</span><span class="sxs-lookup"><span data-stu-id="073b0-137">**November**</span></span>](taskschedulerschema-november-monthstype-element.md)   | <span data-ttu-id="073b0-138">N/D</span><span class="sxs-lookup"><span data-stu-id="073b0-138">N/A</span></span>  | <span data-ttu-id="073b0-139">Especifica que la tarea se ejecuta en noviembre.</span><span class="sxs-lookup"><span data-stu-id="073b0-139">Specifies that the task runs in November.</span></span> <br/>  |
| [<span data-ttu-id="073b0-140">**Octubre**</span><span class="sxs-lookup"><span data-stu-id="073b0-140">**October**</span></span>](taskschedulerschema-october-monthstype-element.md)     | <span data-ttu-id="073b0-141">N/D</span><span class="sxs-lookup"><span data-stu-id="073b0-141">N/A</span></span>  | <span data-ttu-id="073b0-142">Especifica que la tarea se ejecuta en octubre.</span><span class="sxs-lookup"><span data-stu-id="073b0-142">Specifies that the task runs in October.</span></span> <br/>   |
| [<span data-ttu-id="073b0-143">**Septiembre**</span><span class="sxs-lookup"><span data-stu-id="073b0-143">**September**</span></span>](taskschedulerschema-september-monthstype-element.md) | <span data-ttu-id="073b0-144">N/D</span><span class="sxs-lookup"><span data-stu-id="073b0-144">N/A</span></span>  | <span data-ttu-id="073b0-145">Especifica que la tarea se ejecuta en septiembre.</span><span class="sxs-lookup"><span data-stu-id="073b0-145">Specifies that the task runs in September.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="073b0-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="073b0-146">Requirements</span></span>



| <span data-ttu-id="073b0-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="073b0-147">Requirement</span></span> | <span data-ttu-id="073b0-148">Value</span><span class="sxs-lookup"><span data-stu-id="073b0-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="073b0-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="073b0-149">Minimum supported client</span></span><br/> | <span data-ttu-id="073b0-150">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="073b0-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="073b0-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="073b0-151">Minimum supported server</span></span><br/> | <span data-ttu-id="073b0-152">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="073b0-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="073b0-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="073b0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="073b0-154">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="073b0-154">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="073b0-155">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="073b0-155">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





