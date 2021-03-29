---
title: MonthlyDOWTrigger. DaysOfWeek (propiedad)
description: En el caso de scripting, obtiene o establece los días de la semana en los que se ejecuta la tarea.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- Propiedad DaysOfWeek Programador de tareas
- Propiedad DaysOfWeek Programador de tareas, objeto MonthlyDOWTrigger
- Programador de tareas de objeto MonthlyDOWTrigger, propiedad DaysOfWeek
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15344650dabdec2bcbacf91397b37b97ce3f0772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492310"
---
# <a name="monthlydowtriggerdaysofweek-property"></a><span data-ttu-id="247af-106">MonthlyDOWTrigger. DaysOfWeek (propiedad)</span><span class="sxs-lookup"><span data-stu-id="247af-106">MonthlyDOWTrigger.DaysOfWeek property</span></span>

<span data-ttu-id="247af-107">En el caso de scripting, obtiene o establece los días de la semana en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="247af-107">For scripting, gets or sets the days of the week during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="247af-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="247af-108">Syntax</span></span>


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a><span data-ttu-id="247af-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="247af-109">Property value</span></span>

<span data-ttu-id="247af-110">Máscara bit a bit que indica los días de la semana en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="247af-110">A bitwise mask that indicates the days of the week during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="247af-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="247af-111">Remarks</span></span>

<span data-ttu-id="247af-112">En la tabla siguiente se muestra la asignación de la máscara bit a bit utilizada por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="247af-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="247af-113">Día de la semana</span><span class="sxs-lookup"><span data-stu-id="247af-113">Day of Week</span></span> | <span data-ttu-id="247af-114">Valor hexadecimal</span><span class="sxs-lookup"><span data-stu-id="247af-114">Hex Value</span></span> | <span data-ttu-id="247af-115">Valor decimal</span><span class="sxs-lookup"><span data-stu-id="247af-115">Decimal Value</span></span> |
|-------------|-----------|---------------|
| <span data-ttu-id="247af-116">Domingo</span><span class="sxs-lookup"><span data-stu-id="247af-116">Sunday</span></span>      | <span data-ttu-id="247af-117">0x01</span><span class="sxs-lookup"><span data-stu-id="247af-117">0x01</span></span>      | <span data-ttu-id="247af-118">1</span><span class="sxs-lookup"><span data-stu-id="247af-118">1</span></span>             |
| <span data-ttu-id="247af-119">Lunes</span><span class="sxs-lookup"><span data-stu-id="247af-119">Monday</span></span>      | <span data-ttu-id="247af-120">0x02</span><span class="sxs-lookup"><span data-stu-id="247af-120">0x02</span></span>      | <span data-ttu-id="247af-121">2</span><span class="sxs-lookup"><span data-stu-id="247af-121">2</span></span>             |
| <span data-ttu-id="247af-122">Martes</span><span class="sxs-lookup"><span data-stu-id="247af-122">Tuesday</span></span>     | <span data-ttu-id="247af-123">0x04</span><span class="sxs-lookup"><span data-stu-id="247af-123">0x04</span></span>      | <span data-ttu-id="247af-124">4</span><span class="sxs-lookup"><span data-stu-id="247af-124">4</span></span>             |
| <span data-ttu-id="247af-125">Miércoles</span><span class="sxs-lookup"><span data-stu-id="247af-125">Wednesday</span></span>   | <span data-ttu-id="247af-126">0x08</span><span class="sxs-lookup"><span data-stu-id="247af-126">0x08</span></span>      | <span data-ttu-id="247af-127">8</span><span class="sxs-lookup"><span data-stu-id="247af-127">8</span></span>             |
| <span data-ttu-id="247af-128">Jueves</span><span class="sxs-lookup"><span data-stu-id="247af-128">Thursday</span></span>    | <span data-ttu-id="247af-129">0x10</span><span class="sxs-lookup"><span data-stu-id="247af-129">0x10</span></span>      | <span data-ttu-id="247af-130">16</span><span class="sxs-lookup"><span data-stu-id="247af-130">16</span></span>            |
| <span data-ttu-id="247af-131">Viernes</span><span class="sxs-lookup"><span data-stu-id="247af-131">Friday</span></span>      | <span data-ttu-id="247af-132">0x20</span><span class="sxs-lookup"><span data-stu-id="247af-132">0x20</span></span>      | <span data-ttu-id="247af-133">32</span><span class="sxs-lookup"><span data-stu-id="247af-133">32</span></span>            |
| <span data-ttu-id="247af-134">Sábado</span><span class="sxs-lookup"><span data-stu-id="247af-134">Saturday</span></span>    | <span data-ttu-id="247af-135">0x40</span><span class="sxs-lookup"><span data-stu-id="247af-135">0x40</span></span>      | <span data-ttu-id="247af-136">64</span><span class="sxs-lookup"><span data-stu-id="247af-136">64</span></span>            |



 

<span data-ttu-id="247af-137">Al leer o escribir XML para una tarea, los días de la semana de un calendario mensual de día de la semana se especifican mediante el elemento [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="247af-137">When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="247af-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="247af-138">Requirements</span></span>



| <span data-ttu-id="247af-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="247af-139">Requirement</span></span> | <span data-ttu-id="247af-140">Value</span><span class="sxs-lookup"><span data-stu-id="247af-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="247af-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="247af-141">Minimum supported client</span></span><br/> | <span data-ttu-id="247af-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="247af-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="247af-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="247af-143">Minimum supported server</span></span><br/> | <span data-ttu-id="247af-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="247af-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="247af-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="247af-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="247af-146"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="247af-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="247af-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="247af-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="247af-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="247af-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="247af-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="247af-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="247af-150">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="247af-150">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="247af-151">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="247af-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





