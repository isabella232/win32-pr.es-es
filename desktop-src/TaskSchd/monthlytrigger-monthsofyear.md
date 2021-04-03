---
title: Propiedad MonthlyTrigger. MonthsOfYear
description: En el caso de scripting, obtiene o establece los meses del año en los que se ejecuta la tarea. | Propiedad MonthlyTrigger. MonthsOfYear
ms.assetid: cf26a815-7f4f-4b7a-8db8-a4bd9b77cf49
keywords:
- Programador de tareas de la propiedad MonthsOfYear
- Programador de tareas de la propiedad MonthsOfYear, objeto MonthlyTrigger
- Programador de tareas de objeto MonthlyTrigger, propiedad MonthsOfYear
topic_type:
- apiref
api_name:
- MonthlyTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5683fb1c85e470ca7c82b069929de0351ea7cffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914497"
---
# <a name="monthlytriggermonthsofyear-property"></a><span data-ttu-id="24a43-107">Propiedad MonthlyTrigger. MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="24a43-107">MonthlyTrigger.MonthsOfYear property</span></span>

<span data-ttu-id="24a43-108">En el caso de scripting, obtiene o establece los meses del año en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="24a43-108">For scripting, gets or sets the months of the year during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a43-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24a43-109">Syntax</span></span>


```VB
MonthlyTrigger.MonthsOfYear As short
```



## <a name="property-value"></a><span data-ttu-id="24a43-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="24a43-110">Property value</span></span>

<span data-ttu-id="24a43-111">Máscara bit a bit que indica los meses del año en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="24a43-111">A bitwise mask that indicates the months of the year during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="24a43-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24a43-112">Remarks</span></span>

<span data-ttu-id="24a43-113">En la tabla siguiente se muestra la asignación de la máscara bit a bit usada por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="24a43-113">The following table shows the mapping of the bitwise mask that is used by this property.</span></span>



| <span data-ttu-id="24a43-114">Mes</span><span class="sxs-lookup"><span data-stu-id="24a43-114">Month</span></span>     | <span data-ttu-id="24a43-115">Valor hexadecimal</span><span class="sxs-lookup"><span data-stu-id="24a43-115">Hex value</span></span> | <span data-ttu-id="24a43-116">Valor decimal</span><span class="sxs-lookup"><span data-stu-id="24a43-116">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="24a43-117">January</span><span class="sxs-lookup"><span data-stu-id="24a43-117">January</span></span>   | <span data-ttu-id="24a43-118">0X01</span><span class="sxs-lookup"><span data-stu-id="24a43-118">0X01</span></span>      | <span data-ttu-id="24a43-119">1</span><span class="sxs-lookup"><span data-stu-id="24a43-119">1</span></span>             |
| <span data-ttu-id="24a43-120">February</span><span class="sxs-lookup"><span data-stu-id="24a43-120">February</span></span>  | <span data-ttu-id="24a43-121">0x02</span><span class="sxs-lookup"><span data-stu-id="24a43-121">0x02</span></span>      | <span data-ttu-id="24a43-122">2</span><span class="sxs-lookup"><span data-stu-id="24a43-122">2</span></span>             |
| <span data-ttu-id="24a43-123">Marzo</span><span class="sxs-lookup"><span data-stu-id="24a43-123">March</span></span>     | <span data-ttu-id="24a43-124">0X04</span><span class="sxs-lookup"><span data-stu-id="24a43-124">0X04</span></span>      | <span data-ttu-id="24a43-125">4</span><span class="sxs-lookup"><span data-stu-id="24a43-125">4</span></span>             |
| <span data-ttu-id="24a43-126">April</span><span class="sxs-lookup"><span data-stu-id="24a43-126">April</span></span>     | <span data-ttu-id="24a43-127">0X08</span><span class="sxs-lookup"><span data-stu-id="24a43-127">0X08</span></span>      | <span data-ttu-id="24a43-128">8</span><span class="sxs-lookup"><span data-stu-id="24a43-128">8</span></span>             |
| <span data-ttu-id="24a43-129">May</span><span class="sxs-lookup"><span data-stu-id="24a43-129">May</span></span>       | <span data-ttu-id="24a43-130">0X10</span><span class="sxs-lookup"><span data-stu-id="24a43-130">0X10</span></span>      | <span data-ttu-id="24a43-131">16</span><span class="sxs-lookup"><span data-stu-id="24a43-131">16</span></span>            |
| <span data-ttu-id="24a43-132">Junio</span><span class="sxs-lookup"><span data-stu-id="24a43-132">June</span></span>      | <span data-ttu-id="24a43-133">0X20</span><span class="sxs-lookup"><span data-stu-id="24a43-133">0X20</span></span>      | <span data-ttu-id="24a43-134">32</span><span class="sxs-lookup"><span data-stu-id="24a43-134">32</span></span>            |
| <span data-ttu-id="24a43-135">Julio</span><span class="sxs-lookup"><span data-stu-id="24a43-135">July</span></span>      | <span data-ttu-id="24a43-136">0x40</span><span class="sxs-lookup"><span data-stu-id="24a43-136">0x40</span></span>      | <span data-ttu-id="24a43-137">64</span><span class="sxs-lookup"><span data-stu-id="24a43-137">64</span></span>            |
| <span data-ttu-id="24a43-138">Agosto</span><span class="sxs-lookup"><span data-stu-id="24a43-138">August</span></span>    | <span data-ttu-id="24a43-139">0X80</span><span class="sxs-lookup"><span data-stu-id="24a43-139">0X80</span></span>      | <span data-ttu-id="24a43-140">128</span><span class="sxs-lookup"><span data-stu-id="24a43-140">128</span></span>           |
| <span data-ttu-id="24a43-141">Septiembre</span><span class="sxs-lookup"><span data-stu-id="24a43-141">September</span></span> | <span data-ttu-id="24a43-142">0X100</span><span class="sxs-lookup"><span data-stu-id="24a43-142">0X100</span></span>     | <span data-ttu-id="24a43-143">256</span><span class="sxs-lookup"><span data-stu-id="24a43-143">256</span></span>           |
| <span data-ttu-id="24a43-144">Octubre</span><span class="sxs-lookup"><span data-stu-id="24a43-144">October</span></span>   | <span data-ttu-id="24a43-145">0X200</span><span class="sxs-lookup"><span data-stu-id="24a43-145">0X200</span></span>     | <span data-ttu-id="24a43-146">512</span><span class="sxs-lookup"><span data-stu-id="24a43-146">512</span></span>           |
| <span data-ttu-id="24a43-147">Noviembre</span><span class="sxs-lookup"><span data-stu-id="24a43-147">November</span></span>  | <span data-ttu-id="24a43-148">0X400</span><span class="sxs-lookup"><span data-stu-id="24a43-148">0X400</span></span>     | <span data-ttu-id="24a43-149">1024</span><span class="sxs-lookup"><span data-stu-id="24a43-149">1024</span></span>          |
| <span data-ttu-id="24a43-150">Diciembre</span><span class="sxs-lookup"><span data-stu-id="24a43-150">December</span></span>  | <span data-ttu-id="24a43-151">0X800</span><span class="sxs-lookup"><span data-stu-id="24a43-151">0X800</span></span>     | <span data-ttu-id="24a43-152">2048</span><span class="sxs-lookup"><span data-stu-id="24a43-152">2048</span></span>          |



 

<span data-ttu-id="24a43-153">Al leer o escribir su propio XML para una tarea, los meses del año se especifican mediante el elemento [**months**](taskschedulerschema-months-monthlyscheduletype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="24a43-153">When reading or writing your own XML for a task, the months of the year are specified using the [**Months**](taskschedulerschema-months-monthlyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="24a43-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24a43-154">Requirements</span></span>



| <span data-ttu-id="24a43-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="24a43-155">Requirement</span></span> | <span data-ttu-id="24a43-156">Value</span><span class="sxs-lookup"><span data-stu-id="24a43-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24a43-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24a43-157">Minimum supported client</span></span><br/> | <span data-ttu-id="24a43-158">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="24a43-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="24a43-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24a43-159">Minimum supported server</span></span><br/> | <span data-ttu-id="24a43-160">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="24a43-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="24a43-161">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="24a43-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="24a43-162"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="24a43-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="24a43-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="24a43-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24a43-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24a43-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24a43-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="24a43-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a43-166">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="24a43-166">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="24a43-167">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="24a43-167">**MonthlyTrigger**</span></span>](monthlytrigger.md)
</dt> </dl>

 

 





