---
title: Propiedad MonthlyTrigger. DaysOfMonth
description: En el caso de scripting, obtiene o establece los días del mes durante los que se ejecuta la tarea.
ms.assetid: 4da80d0f-ae0c-4e56-b51b-6ee6ab309d7c
keywords:
- Programador de tareas de la propiedad DaysOfMonth
- Programador de tareas de la propiedad DaysOfMonth, objeto MonthlyTrigger
- Programador de tareas de objeto MonthlyTrigger, propiedad DaysOfMonth
topic_type:
- apiref
api_name:
- MonthlyTrigger.DaysOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a3bd671266cfbe459218367fadf20fd52f94a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150512"
---
# <a name="monthlytriggerdaysofmonth-property"></a><span data-ttu-id="8d511-106">Propiedad MonthlyTrigger. DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="8d511-106">MonthlyTrigger.DaysOfMonth property</span></span>

<span data-ttu-id="8d511-107">En el caso de scripting, obtiene o establece los días del mes durante los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="8d511-107">For scripting, gets or sets the days of the month during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d511-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d511-108">Syntax</span></span>


```VB
MonthlyTrigger.DaysOfMonth As long
```



## <a name="property-value"></a><span data-ttu-id="8d511-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8d511-109">Property value</span></span>

<span data-ttu-id="8d511-110">Máscara bit a bit que indica los días del mes en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="8d511-110">A bitwise mask that indicates the days of the month during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d511-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d511-111">Remarks</span></span>



| <span data-ttu-id="8d511-112">Día del mes.</span><span class="sxs-lookup"><span data-stu-id="8d511-112">Day of month</span></span> | <span data-ttu-id="8d511-113">Valor hexadecimal</span><span class="sxs-lookup"><span data-stu-id="8d511-113">Hex value</span></span>  | <span data-ttu-id="8d511-114">Valor decimal</span><span class="sxs-lookup"><span data-stu-id="8d511-114">Decimal value</span></span> |
|--------------|------------|---------------|
| <span data-ttu-id="8d511-115">1</span><span class="sxs-lookup"><span data-stu-id="8d511-115">1</span></span>            | <span data-ttu-id="8d511-116">0x01</span><span class="sxs-lookup"><span data-stu-id="8d511-116">0x01</span></span>       | <span data-ttu-id="8d511-117">1</span><span class="sxs-lookup"><span data-stu-id="8d511-117">1</span></span>             |
| <span data-ttu-id="8d511-118">2</span><span class="sxs-lookup"><span data-stu-id="8d511-118">2</span></span>            | <span data-ttu-id="8d511-119">0x02</span><span class="sxs-lookup"><span data-stu-id="8d511-119">0x02</span></span>       | <span data-ttu-id="8d511-120">2</span><span class="sxs-lookup"><span data-stu-id="8d511-120">2</span></span>             |
| <span data-ttu-id="8d511-121">3</span><span class="sxs-lookup"><span data-stu-id="8d511-121">3</span></span>            | <span data-ttu-id="8d511-122">0x04</span><span class="sxs-lookup"><span data-stu-id="8d511-122">0x04</span></span>       | <span data-ttu-id="8d511-123">4</span><span class="sxs-lookup"><span data-stu-id="8d511-123">4</span></span>             |
| <span data-ttu-id="8d511-124">4</span><span class="sxs-lookup"><span data-stu-id="8d511-124">4</span></span>            | <span data-ttu-id="8d511-125">0x08</span><span class="sxs-lookup"><span data-stu-id="8d511-125">0x08</span></span>       | <span data-ttu-id="8d511-126">8</span><span class="sxs-lookup"><span data-stu-id="8d511-126">8</span></span>             |
| <span data-ttu-id="8d511-127">5</span><span class="sxs-lookup"><span data-stu-id="8d511-127">5</span></span>            | <span data-ttu-id="8d511-128">0x10</span><span class="sxs-lookup"><span data-stu-id="8d511-128">0x10</span></span>       | <span data-ttu-id="8d511-129">16</span><span class="sxs-lookup"><span data-stu-id="8d511-129">16</span></span>            |
| <span data-ttu-id="8d511-130">6</span><span class="sxs-lookup"><span data-stu-id="8d511-130">6</span></span>            | <span data-ttu-id="8d511-131">0x20</span><span class="sxs-lookup"><span data-stu-id="8d511-131">0x20</span></span>       | <span data-ttu-id="8d511-132">32</span><span class="sxs-lookup"><span data-stu-id="8d511-132">32</span></span>            |
| <span data-ttu-id="8d511-133">7</span><span class="sxs-lookup"><span data-stu-id="8d511-133">7</span></span>            | <span data-ttu-id="8d511-134">0x40</span><span class="sxs-lookup"><span data-stu-id="8d511-134">0x40</span></span>       | <span data-ttu-id="8d511-135">64</span><span class="sxs-lookup"><span data-stu-id="8d511-135">64</span></span>            |
| <span data-ttu-id="8d511-136">8</span><span class="sxs-lookup"><span data-stu-id="8d511-136">8</span></span>            | <span data-ttu-id="8d511-137">0x80</span><span class="sxs-lookup"><span data-stu-id="8d511-137">0x80</span></span>       | <span data-ttu-id="8d511-138">128</span><span class="sxs-lookup"><span data-stu-id="8d511-138">128</span></span>           |
| <span data-ttu-id="8d511-139">9</span><span class="sxs-lookup"><span data-stu-id="8d511-139">9</span></span>            | <span data-ttu-id="8d511-140">0x100</span><span class="sxs-lookup"><span data-stu-id="8d511-140">0x100</span></span>      | <span data-ttu-id="8d511-141">256</span><span class="sxs-lookup"><span data-stu-id="8d511-141">256</span></span>           |
| <span data-ttu-id="8d511-142">10</span><span class="sxs-lookup"><span data-stu-id="8d511-142">10</span></span>           | <span data-ttu-id="8d511-143">0x200</span><span class="sxs-lookup"><span data-stu-id="8d511-143">0x200</span></span>      | <span data-ttu-id="8d511-144">512</span><span class="sxs-lookup"><span data-stu-id="8d511-144">512</span></span>           |
| <span data-ttu-id="8d511-145">11</span><span class="sxs-lookup"><span data-stu-id="8d511-145">11</span></span>           | <span data-ttu-id="8d511-146">0x400</span><span class="sxs-lookup"><span data-stu-id="8d511-146">0x400</span></span>      | <span data-ttu-id="8d511-147">1024</span><span class="sxs-lookup"><span data-stu-id="8d511-147">1024</span></span>          |
| <span data-ttu-id="8d511-148">12</span><span class="sxs-lookup"><span data-stu-id="8d511-148">12</span></span>           | <span data-ttu-id="8d511-149">0x800</span><span class="sxs-lookup"><span data-stu-id="8d511-149">0x800</span></span>      | <span data-ttu-id="8d511-150">2048</span><span class="sxs-lookup"><span data-stu-id="8d511-150">2048</span></span>          |
| <span data-ttu-id="8d511-151">13</span><span class="sxs-lookup"><span data-stu-id="8d511-151">13</span></span>           | <span data-ttu-id="8d511-152">0x1000</span><span class="sxs-lookup"><span data-stu-id="8d511-152">0x1000</span></span>     | <span data-ttu-id="8d511-153">4096</span><span class="sxs-lookup"><span data-stu-id="8d511-153">4096</span></span>          |
| <span data-ttu-id="8d511-154">14</span><span class="sxs-lookup"><span data-stu-id="8d511-154">14</span></span>           | <span data-ttu-id="8d511-155">0x2000</span><span class="sxs-lookup"><span data-stu-id="8d511-155">0x2000</span></span>     | <span data-ttu-id="8d511-156">8192</span><span class="sxs-lookup"><span data-stu-id="8d511-156">8192</span></span>          |
| <span data-ttu-id="8d511-157">15</span><span class="sxs-lookup"><span data-stu-id="8d511-157">15</span></span>           | <span data-ttu-id="8d511-158">0x4000</span><span class="sxs-lookup"><span data-stu-id="8d511-158">0x4000</span></span>     | <span data-ttu-id="8d511-159">16384</span><span class="sxs-lookup"><span data-stu-id="8d511-159">16384</span></span>         |
| <span data-ttu-id="8d511-160">16</span><span class="sxs-lookup"><span data-stu-id="8d511-160">16</span></span>           | <span data-ttu-id="8d511-161">0x8000</span><span class="sxs-lookup"><span data-stu-id="8d511-161">0x8000</span></span>     | <span data-ttu-id="8d511-162">32 768</span><span class="sxs-lookup"><span data-stu-id="8d511-162">32768</span></span>         |
| <span data-ttu-id="8d511-163">17</span><span class="sxs-lookup"><span data-stu-id="8d511-163">17</span></span>           | <span data-ttu-id="8d511-164">0x10000</span><span class="sxs-lookup"><span data-stu-id="8d511-164">0x10000</span></span>    | <span data-ttu-id="8d511-165">65536</span><span class="sxs-lookup"><span data-stu-id="8d511-165">65536</span></span>         |
| <span data-ttu-id="8d511-166">18</span><span class="sxs-lookup"><span data-stu-id="8d511-166">18</span></span>           | <span data-ttu-id="8d511-167">0x20000</span><span class="sxs-lookup"><span data-stu-id="8d511-167">0x20000</span></span>    | <span data-ttu-id="8d511-168">131 072</span><span class="sxs-lookup"><span data-stu-id="8d511-168">131072</span></span>        |
| <span data-ttu-id="8d511-169">19</span><span class="sxs-lookup"><span data-stu-id="8d511-169">19</span></span>           | <span data-ttu-id="8d511-170">0x40000</span><span class="sxs-lookup"><span data-stu-id="8d511-170">0x40000</span></span>    | <span data-ttu-id="8d511-171">262 144</span><span class="sxs-lookup"><span data-stu-id="8d511-171">262144</span></span>        |
| <span data-ttu-id="8d511-172">20</span><span class="sxs-lookup"><span data-stu-id="8d511-172">20</span></span>           | <span data-ttu-id="8d511-173">0x80000</span><span class="sxs-lookup"><span data-stu-id="8d511-173">0x80000</span></span>    | <span data-ttu-id="8d511-174">524 288</span><span class="sxs-lookup"><span data-stu-id="8d511-174">524288</span></span>        |
| <span data-ttu-id="8d511-175">21</span><span class="sxs-lookup"><span data-stu-id="8d511-175">21</span></span>           | <span data-ttu-id="8d511-176">0x100000</span><span class="sxs-lookup"><span data-stu-id="8d511-176">0x100000</span></span>   | <span data-ttu-id="8d511-177">1 048 576</span><span class="sxs-lookup"><span data-stu-id="8d511-177">1048576</span></span>       |
| <span data-ttu-id="8d511-178">22</span><span class="sxs-lookup"><span data-stu-id="8d511-178">22</span></span>           | <span data-ttu-id="8d511-179">0x200000</span><span class="sxs-lookup"><span data-stu-id="8d511-179">0x200000</span></span>   | <span data-ttu-id="8d511-180">2 097 152</span><span class="sxs-lookup"><span data-stu-id="8d511-180">2097152</span></span>       |
| <span data-ttu-id="8d511-181">23</span><span class="sxs-lookup"><span data-stu-id="8d511-181">23</span></span>           | <span data-ttu-id="8d511-182">0x400000</span><span class="sxs-lookup"><span data-stu-id="8d511-182">0x400000</span></span>   | <span data-ttu-id="8d511-183">4 194 304</span><span class="sxs-lookup"><span data-stu-id="8d511-183">4194304</span></span>       |
| <span data-ttu-id="8d511-184">24</span><span class="sxs-lookup"><span data-stu-id="8d511-184">24</span></span>           | <span data-ttu-id="8d511-185">0x800000</span><span class="sxs-lookup"><span data-stu-id="8d511-185">0x800000</span></span>   | <span data-ttu-id="8d511-186">8388608</span><span class="sxs-lookup"><span data-stu-id="8d511-186">8388608</span></span>       |
| <span data-ttu-id="8d511-187">25</span><span class="sxs-lookup"><span data-stu-id="8d511-187">25</span></span>           | <span data-ttu-id="8d511-188">0x1000000</span><span class="sxs-lookup"><span data-stu-id="8d511-188">0x1000000</span></span>  | <span data-ttu-id="8d511-189">16777216</span><span class="sxs-lookup"><span data-stu-id="8d511-189">16777216</span></span>      |
| <span data-ttu-id="8d511-190">26</span><span class="sxs-lookup"><span data-stu-id="8d511-190">26</span></span>           | <span data-ttu-id="8d511-191">0x2000000</span><span class="sxs-lookup"><span data-stu-id="8d511-191">0x2000000</span></span>  | <span data-ttu-id="8d511-192">33554432</span><span class="sxs-lookup"><span data-stu-id="8d511-192">33554432</span></span>      |
| <span data-ttu-id="8d511-193">27</span><span class="sxs-lookup"><span data-stu-id="8d511-193">27</span></span>           | <span data-ttu-id="8d511-194">0x4000000</span><span class="sxs-lookup"><span data-stu-id="8d511-194">0x4000000</span></span>  | <span data-ttu-id="8d511-195">67108864</span><span class="sxs-lookup"><span data-stu-id="8d511-195">67108864</span></span>      |
| <span data-ttu-id="8d511-196">28</span><span class="sxs-lookup"><span data-stu-id="8d511-196">28</span></span>           | <span data-ttu-id="8d511-197">0x8000000</span><span class="sxs-lookup"><span data-stu-id="8d511-197">0x8000000</span></span>  | <span data-ttu-id="8d511-198">134217728</span><span class="sxs-lookup"><span data-stu-id="8d511-198">134217728</span></span>     |
| <span data-ttu-id="8d511-199">29</span><span class="sxs-lookup"><span data-stu-id="8d511-199">29</span></span>           | <span data-ttu-id="8d511-200">0x10000000</span><span class="sxs-lookup"><span data-stu-id="8d511-200">0x10000000</span></span> | <span data-ttu-id="8d511-201">268435456</span><span class="sxs-lookup"><span data-stu-id="8d511-201">268435456</span></span>     |
| <span data-ttu-id="8d511-202">30</span><span class="sxs-lookup"><span data-stu-id="8d511-202">30</span></span>           | <span data-ttu-id="8d511-203">0x20000000</span><span class="sxs-lookup"><span data-stu-id="8d511-203">0x20000000</span></span> | <span data-ttu-id="8d511-204">536870912</span><span class="sxs-lookup"><span data-stu-id="8d511-204">536870912</span></span>     |
| <span data-ttu-id="8d511-205">31</span><span class="sxs-lookup"><span data-stu-id="8d511-205">31</span></span>           | <span data-ttu-id="8d511-206">0x40000000</span><span class="sxs-lookup"><span data-stu-id="8d511-206">0x40000000</span></span> | <span data-ttu-id="8d511-207">1073741824</span><span class="sxs-lookup"><span data-stu-id="8d511-207">1073741824</span></span>    |
| <span data-ttu-id="8d511-208">Último</span><span class="sxs-lookup"><span data-stu-id="8d511-208">Last</span></span>         | <span data-ttu-id="8d511-209">0x80000000</span><span class="sxs-lookup"><span data-stu-id="8d511-209">0x80000000</span></span> | <span data-ttu-id="8d511-210">2147483648</span><span class="sxs-lookup"><span data-stu-id="8d511-210">2147483648</span></span>    |



 

<span data-ttu-id="8d511-211">Al leer o escribir su propio XML para una tarea, los días del mes se especifican mediante el elemento [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="8d511-211">When reading or writing your own XML for a task, the days of the month are specified using the [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d511-212">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d511-212">Requirements</span></span>



| <span data-ttu-id="8d511-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d511-213">Requirement</span></span> | <span data-ttu-id="8d511-214">Value</span><span class="sxs-lookup"><span data-stu-id="8d511-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d511-215">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d511-215">Minimum supported client</span></span><br/> | <span data-ttu-id="8d511-216">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8d511-216">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8d511-217">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d511-217">Minimum supported server</span></span><br/> | <span data-ttu-id="8d511-218">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d511-218">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8d511-219">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8d511-219">Type library</span></span><br/>             | <dl> <span data-ttu-id="8d511-220"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8d511-220"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8d511-221">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8d511-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d511-222"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d511-222"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d511-223">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d511-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d511-224">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="8d511-224">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="8d511-225">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="8d511-225">**MonthlyTrigger**</span></span>](monthlytrigger.md)
</dt> </dl>

 

 





