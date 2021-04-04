---
title: Propiedad MonthlyDOWTrigger. MonthsOfYear
description: En el caso de scripting, obtiene o establece los meses del año en los que se ejecuta la tarea. | Propiedad MonthlyDOWTrigger. MonthsOfYear
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- Programador de tareas de la propiedad MonthsOfYear
- Programador de tareas de la propiedad MonthsOfYear, objeto MonthlyDOWTrigger
- Programador de tareas de objeto MonthlyDOWTrigger, propiedad MonthsOfYear
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c345cd3de12d7dba3450f62bdb18bfdcee496b13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914597"
---
# <a name="monthlydowtriggermonthsofyear-property"></a><span data-ttu-id="8d5da-107">Propiedad MonthlyDOWTrigger. MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="8d5da-107">MonthlyDOWTrigger.MonthsOfYear property</span></span>

<span data-ttu-id="8d5da-108">En el caso de scripting, obtiene o establece los meses del año en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="8d5da-108">For scripting, gets or sets the months of the year during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d5da-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d5da-109">Syntax</span></span>


```VB
MonthlyDOWTrigger.MonthsOfYear As short
```



## <a name="property-value"></a><span data-ttu-id="8d5da-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8d5da-110">Property value</span></span>

<span data-ttu-id="8d5da-111">Máscara bit a bit que indica los meses del año en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="8d5da-111">A bitwise mask that indicates the months of the year during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d5da-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d5da-112">Remarks</span></span>

<span data-ttu-id="8d5da-113">En la tabla siguiente se muestra la asignación de la máscara bit a bit utilizada por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="8d5da-113">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="8d5da-114">Mes</span><span class="sxs-lookup"><span data-stu-id="8d5da-114">Month</span></span>     | <span data-ttu-id="8d5da-115">Valor hexadecimal</span><span class="sxs-lookup"><span data-stu-id="8d5da-115">Hex value</span></span> | <span data-ttu-id="8d5da-116">Valor decimal</span><span class="sxs-lookup"><span data-stu-id="8d5da-116">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="8d5da-117">January</span><span class="sxs-lookup"><span data-stu-id="8d5da-117">January</span></span>   | <span data-ttu-id="8d5da-118">0X01</span><span class="sxs-lookup"><span data-stu-id="8d5da-118">0X01</span></span>      | <span data-ttu-id="8d5da-119">1</span><span class="sxs-lookup"><span data-stu-id="8d5da-119">1</span></span>             |
| <span data-ttu-id="8d5da-120">February</span><span class="sxs-lookup"><span data-stu-id="8d5da-120">February</span></span>  | <span data-ttu-id="8d5da-121">0x02</span><span class="sxs-lookup"><span data-stu-id="8d5da-121">0x02</span></span>      | <span data-ttu-id="8d5da-122">2</span><span class="sxs-lookup"><span data-stu-id="8d5da-122">2</span></span>             |
| <span data-ttu-id="8d5da-123">Marzo</span><span class="sxs-lookup"><span data-stu-id="8d5da-123">March</span></span>     | <span data-ttu-id="8d5da-124">0X04</span><span class="sxs-lookup"><span data-stu-id="8d5da-124">0X04</span></span>      | <span data-ttu-id="8d5da-125">4</span><span class="sxs-lookup"><span data-stu-id="8d5da-125">4</span></span>             |
| <span data-ttu-id="8d5da-126">April</span><span class="sxs-lookup"><span data-stu-id="8d5da-126">April</span></span>     | <span data-ttu-id="8d5da-127">0X08</span><span class="sxs-lookup"><span data-stu-id="8d5da-127">0X08</span></span>      | <span data-ttu-id="8d5da-128">8</span><span class="sxs-lookup"><span data-stu-id="8d5da-128">8</span></span>             |
| <span data-ttu-id="8d5da-129">May</span><span class="sxs-lookup"><span data-stu-id="8d5da-129">May</span></span>       | <span data-ttu-id="8d5da-130">0X10</span><span class="sxs-lookup"><span data-stu-id="8d5da-130">0X10</span></span>      | <span data-ttu-id="8d5da-131">16</span><span class="sxs-lookup"><span data-stu-id="8d5da-131">16</span></span>            |
| <span data-ttu-id="8d5da-132">Junio</span><span class="sxs-lookup"><span data-stu-id="8d5da-132">June</span></span>      | <span data-ttu-id="8d5da-133">0X20</span><span class="sxs-lookup"><span data-stu-id="8d5da-133">0X20</span></span>      | <span data-ttu-id="8d5da-134">32</span><span class="sxs-lookup"><span data-stu-id="8d5da-134">32</span></span>            |
| <span data-ttu-id="8d5da-135">Julio</span><span class="sxs-lookup"><span data-stu-id="8d5da-135">July</span></span>      | <span data-ttu-id="8d5da-136">0x40</span><span class="sxs-lookup"><span data-stu-id="8d5da-136">0x40</span></span>      | <span data-ttu-id="8d5da-137">64</span><span class="sxs-lookup"><span data-stu-id="8d5da-137">64</span></span>            |
| <span data-ttu-id="8d5da-138">Agosto</span><span class="sxs-lookup"><span data-stu-id="8d5da-138">August</span></span>    | <span data-ttu-id="8d5da-139">0X80</span><span class="sxs-lookup"><span data-stu-id="8d5da-139">0X80</span></span>      | <span data-ttu-id="8d5da-140">128</span><span class="sxs-lookup"><span data-stu-id="8d5da-140">128</span></span>           |
| <span data-ttu-id="8d5da-141">Septiembre</span><span class="sxs-lookup"><span data-stu-id="8d5da-141">September</span></span> | <span data-ttu-id="8d5da-142">0X100</span><span class="sxs-lookup"><span data-stu-id="8d5da-142">0X100</span></span>     | <span data-ttu-id="8d5da-143">256</span><span class="sxs-lookup"><span data-stu-id="8d5da-143">256</span></span>           |
| <span data-ttu-id="8d5da-144">Octubre</span><span class="sxs-lookup"><span data-stu-id="8d5da-144">October</span></span>   | <span data-ttu-id="8d5da-145">0X200</span><span class="sxs-lookup"><span data-stu-id="8d5da-145">0X200</span></span>     | <span data-ttu-id="8d5da-146">512</span><span class="sxs-lookup"><span data-stu-id="8d5da-146">512</span></span>           |
| <span data-ttu-id="8d5da-147">Noviembre</span><span class="sxs-lookup"><span data-stu-id="8d5da-147">November</span></span>  | <span data-ttu-id="8d5da-148">0X400</span><span class="sxs-lookup"><span data-stu-id="8d5da-148">0X400</span></span>     | <span data-ttu-id="8d5da-149">1024</span><span class="sxs-lookup"><span data-stu-id="8d5da-149">1024</span></span>          |
| <span data-ttu-id="8d5da-150">Diciembre</span><span class="sxs-lookup"><span data-stu-id="8d5da-150">December</span></span>  | <span data-ttu-id="8d5da-151">0X800</span><span class="sxs-lookup"><span data-stu-id="8d5da-151">0X800</span></span>     | <span data-ttu-id="8d5da-152">2048</span><span class="sxs-lookup"><span data-stu-id="8d5da-152">2048</span></span>          |



 

<span data-ttu-id="8d5da-153">Al leer o escribir XML para una tarea, los meses del año de un calendario mensual de día de la semana se especifican mediante el elemento [**months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="8d5da-153">When reading or writing XML for a task, the months of the year of a monthly day-of-week calendar are specified by the [**Months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d5da-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d5da-154">Requirements</span></span>



| <span data-ttu-id="8d5da-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d5da-155">Requirement</span></span> | <span data-ttu-id="8d5da-156">Value</span><span class="sxs-lookup"><span data-stu-id="8d5da-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d5da-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d5da-157">Minimum supported client</span></span><br/> | <span data-ttu-id="8d5da-158">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8d5da-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8d5da-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d5da-159">Minimum supported server</span></span><br/> | <span data-ttu-id="8d5da-160">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d5da-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8d5da-161">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8d5da-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="8d5da-162"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8d5da-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8d5da-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8d5da-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d5da-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d5da-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d5da-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d5da-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d5da-166">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="8d5da-166">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="8d5da-167">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="8d5da-167">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





