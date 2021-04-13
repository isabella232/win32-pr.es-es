---
title: WeeklyTrigger. DaysOfWeek (propiedad)
description: En el caso de scripting, obtiene o establece los días de la semana en los que se ejecuta la tarea.
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- Propiedad DaysOfWeek Programador de tareas
- Propiedad DaysOfWeek Programador de tareas, objeto WeeklyTrigger
- Programador de tareas de objeto WeeklyTrigger, propiedad DaysOfWeek
topic_type:
- apiref
api_name:
- WeeklyTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f0a27ef031e7baf46d2d3c0e33c23fb505c7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535590"
---
# <a name="weeklytriggerdaysofweek-property"></a><span data-ttu-id="f9fec-106">WeeklyTrigger. DaysOfWeek (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f9fec-106">WeeklyTrigger.DaysOfWeek property</span></span>

<span data-ttu-id="f9fec-107">En el caso de scripting, obtiene o establece los días de la semana en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="f9fec-107">For scripting, gets or sets the days of the week on which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9fec-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9fec-108">Syntax</span></span>


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a><span data-ttu-id="f9fec-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f9fec-109">Property value</span></span>

<span data-ttu-id="f9fec-110">Máscara bit a bit que indica los días de la semana en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="f9fec-110">A bitwise mask that indicates the days of the week on which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9fec-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9fec-111">Remarks</span></span>

<span data-ttu-id="f9fec-112">En la tabla siguiente se muestra la asignación de la máscara bit a bit utilizada por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f9fec-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="f9fec-113">Mes</span><span class="sxs-lookup"><span data-stu-id="f9fec-113">Month</span></span>     | <span data-ttu-id="f9fec-114">Valor hexadecimal</span><span class="sxs-lookup"><span data-stu-id="f9fec-114">Hex value</span></span> | <span data-ttu-id="f9fec-115">Valor decimal</span><span class="sxs-lookup"><span data-stu-id="f9fec-115">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="f9fec-116">Domingo</span><span class="sxs-lookup"><span data-stu-id="f9fec-116">Sunday</span></span>    | <span data-ttu-id="f9fec-117">0X01</span><span class="sxs-lookup"><span data-stu-id="f9fec-117">0X01</span></span>      | <span data-ttu-id="f9fec-118">1</span><span class="sxs-lookup"><span data-stu-id="f9fec-118">1</span></span>             |
| <span data-ttu-id="f9fec-119">Lunes</span><span class="sxs-lookup"><span data-stu-id="f9fec-119">Monday</span></span>    | <span data-ttu-id="f9fec-120">0x02</span><span class="sxs-lookup"><span data-stu-id="f9fec-120">0x02</span></span>      | <span data-ttu-id="f9fec-121">2</span><span class="sxs-lookup"><span data-stu-id="f9fec-121">2</span></span>             |
| <span data-ttu-id="f9fec-122">Martes</span><span class="sxs-lookup"><span data-stu-id="f9fec-122">Tuesday</span></span>   | <span data-ttu-id="f9fec-123">0X04</span><span class="sxs-lookup"><span data-stu-id="f9fec-123">0X04</span></span>      | <span data-ttu-id="f9fec-124">4</span><span class="sxs-lookup"><span data-stu-id="f9fec-124">4</span></span>             |
| <span data-ttu-id="f9fec-125">Miércoles</span><span class="sxs-lookup"><span data-stu-id="f9fec-125">Wednesday</span></span> | <span data-ttu-id="f9fec-126">0X08</span><span class="sxs-lookup"><span data-stu-id="f9fec-126">0X08</span></span>      | <span data-ttu-id="f9fec-127">8</span><span class="sxs-lookup"><span data-stu-id="f9fec-127">8</span></span>             |
| <span data-ttu-id="f9fec-128">Jueves</span><span class="sxs-lookup"><span data-stu-id="f9fec-128">Thursday</span></span>  | <span data-ttu-id="f9fec-129">0X10</span><span class="sxs-lookup"><span data-stu-id="f9fec-129">0X10</span></span>      | <span data-ttu-id="f9fec-130">16</span><span class="sxs-lookup"><span data-stu-id="f9fec-130">16</span></span>            |
| <span data-ttu-id="f9fec-131">Viernes</span><span class="sxs-lookup"><span data-stu-id="f9fec-131">Friday</span></span>    | <span data-ttu-id="f9fec-132">0x20</span><span class="sxs-lookup"><span data-stu-id="f9fec-132">0x20</span></span>      | <span data-ttu-id="f9fec-133">32</span><span class="sxs-lookup"><span data-stu-id="f9fec-133">32</span></span>            |
| <span data-ttu-id="f9fec-134">Sábado</span><span class="sxs-lookup"><span data-stu-id="f9fec-134">Saturday</span></span>  | <span data-ttu-id="f9fec-135">0X40</span><span class="sxs-lookup"><span data-stu-id="f9fec-135">0X40</span></span>      | <span data-ttu-id="f9fec-136">64</span><span class="sxs-lookup"><span data-stu-id="f9fec-136">64</span></span>            |



 

<span data-ttu-id="f9fec-137">Al leer o escribir su propio XML para una tarea, los días de la semana se especifican mediante el elemento [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="f9fec-137">When reading or writing your own XML for a task, the days of the week are specified using the [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9fec-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9fec-138">Requirements</span></span>



| <span data-ttu-id="f9fec-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9fec-139">Requirement</span></span> | <span data-ttu-id="f9fec-140">Value</span><span class="sxs-lookup"><span data-stu-id="f9fec-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9fec-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9fec-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f9fec-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f9fec-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f9fec-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9fec-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f9fec-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f9fec-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f9fec-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f9fec-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="f9fec-146"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f9fec-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f9fec-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9fec-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9fec-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9fec-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9fec-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9fec-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9fec-150">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f9fec-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





