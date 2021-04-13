---
title: Propiedad MonthlyDOWTrigger. WeeksOfMonth
description: En el caso de scripting, obtiene o establece las semanas del mes en las que se ejecuta la tarea.
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- Programador de tareas de la propiedad WeeksOfMonth
- Programador de tareas de la propiedad WeeksOfMonth, objeto MonthlyDOWTrigger
- Programador de tareas de objeto MonthlyDOWTrigger, propiedad WeeksOfMonth
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.WeeksOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7efea628e6eefdef07bdc50b9719a7c404f78bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489700"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a><span data-ttu-id="11508-106">Propiedad MonthlyDOWTrigger. WeeksOfMonth</span><span class="sxs-lookup"><span data-stu-id="11508-106">MonthlyDOWTrigger.WeeksOfMonth property</span></span>

<span data-ttu-id="11508-107">En el caso de scripting, obtiene o establece las semanas del mes en las que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="11508-107">For scripting, gets or sets the weeks of the month during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="11508-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11508-108">Syntax</span></span>


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a><span data-ttu-id="11508-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="11508-109">Property value</span></span>

<span data-ttu-id="11508-110">Máscara bit a bit que indica los días de la semana en los que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="11508-110">A bitwise mask that indicates the days of the week during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="11508-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11508-111">Remarks</span></span>

<span data-ttu-id="11508-112">En la tabla siguiente se muestra la asignación de la máscara bit a bit utilizada por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="11508-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="11508-113">Semana</span><span class="sxs-lookup"><span data-stu-id="11508-113">Week</span></span>                     | <span data-ttu-id="11508-114">Valor hexadecimal</span><span class="sxs-lookup"><span data-stu-id="11508-114">Hex Value</span></span> | <span data-ttu-id="11508-115">Valor decimal</span><span class="sxs-lookup"><span data-stu-id="11508-115">Decimal Value</span></span> |
|--------------------------|-----------|---------------|
| <span data-ttu-id="11508-116">Primera semana del mes</span><span class="sxs-lookup"><span data-stu-id="11508-116">First week of the month</span></span>  | <span data-ttu-id="11508-117">0X01</span><span class="sxs-lookup"><span data-stu-id="11508-117">0X01</span></span>      | <span data-ttu-id="11508-118">1</span><span class="sxs-lookup"><span data-stu-id="11508-118">1</span></span>             |
| <span data-ttu-id="11508-119">Segunda semana del mes</span><span class="sxs-lookup"><span data-stu-id="11508-119">Second week of the month</span></span> | <span data-ttu-id="11508-120">0x02</span><span class="sxs-lookup"><span data-stu-id="11508-120">0x02</span></span>      | <span data-ttu-id="11508-121">2</span><span class="sxs-lookup"><span data-stu-id="11508-121">2</span></span>             |
| <span data-ttu-id="11508-122">Tercera semana del mes</span><span class="sxs-lookup"><span data-stu-id="11508-122">Third week of the month</span></span>  | <span data-ttu-id="11508-123">0X04</span><span class="sxs-lookup"><span data-stu-id="11508-123">0X04</span></span>      | <span data-ttu-id="11508-124">4</span><span class="sxs-lookup"><span data-stu-id="11508-124">4</span></span>             |
| <span data-ttu-id="11508-125">Cuarta semana del mes</span><span class="sxs-lookup"><span data-stu-id="11508-125">Fourth week of the month</span></span> | <span data-ttu-id="11508-126">0X08</span><span class="sxs-lookup"><span data-stu-id="11508-126">0X08</span></span>      | <span data-ttu-id="11508-127">8</span><span class="sxs-lookup"><span data-stu-id="11508-127">8</span></span>             |



 

<span data-ttu-id="11508-128">Al leer o escribir XML para una tarea, los días de la semana de un calendario mensual de día de la semana se especifican mediante el elemento [**weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="11508-128">When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the [**Weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="11508-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11508-129">Requirements</span></span>



| <span data-ttu-id="11508-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="11508-130">Requirement</span></span> | <span data-ttu-id="11508-131">Value</span><span class="sxs-lookup"><span data-stu-id="11508-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11508-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11508-132">Minimum supported client</span></span><br/> | <span data-ttu-id="11508-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="11508-133">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="11508-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11508-134">Minimum supported server</span></span><br/> | <span data-ttu-id="11508-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="11508-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="11508-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="11508-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="11508-137"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="11508-137"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="11508-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="11508-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11508-139"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11508-139"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11508-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="11508-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11508-141">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="11508-141">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="11508-142">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="11508-142">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





