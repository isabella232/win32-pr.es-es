---
title: Propiedad WeeklyTrigger. WeeksInterval
description: En el caso de scripting, obtiene o establece el intervalo entre las semanas de la programación.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- Programador de tareas de la propiedad WeeksInterval
- Programador de tareas de la propiedad WeeksInterval, objeto WeeklyTrigger
- Programador de tareas de objeto WeeklyTrigger, propiedad WeeksInterval
topic_type:
- apiref
api_name:
- WeeklyTrigger.WeeksInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4668b68d0b3f83e096284db35df799a63eb677b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685876"
---
# <a name="weeklytriggerweeksinterval-property"></a><span data-ttu-id="ec7de-106">Propiedad WeeklyTrigger. WeeksInterval</span><span class="sxs-lookup"><span data-stu-id="ec7de-106">WeeklyTrigger.WeeksInterval property</span></span>

<span data-ttu-id="ec7de-107">En el caso de scripting, obtiene o establece el intervalo entre las semanas de la programación.</span><span class="sxs-lookup"><span data-stu-id="ec7de-107">For scripting, gets or sets the interval between the weeks in the schedule.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec7de-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec7de-108">Syntax</span></span>


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a><span data-ttu-id="ec7de-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ec7de-109">Property value</span></span>

<span data-ttu-id="ec7de-110">Intervalo entre las semanas de la programación.</span><span class="sxs-lookup"><span data-stu-id="ec7de-110">The interval between the weeks in the schedule.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec7de-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec7de-111">Remarks</span></span>

<span data-ttu-id="ec7de-112">Un intervalo de 1 genera una programación semanal.</span><span class="sxs-lookup"><span data-stu-id="ec7de-112">An interval of 1 produces a weekly schedule.</span></span> <span data-ttu-id="ec7de-113">Un intervalo de 2 genera una programación de cada semana.</span><span class="sxs-lookup"><span data-stu-id="ec7de-113">An interval of 2 produces an every-other week schedule.</span></span>

<span data-ttu-id="ec7de-114">Al leer o escribir su propio XML para una tarea, el intervalo de una programación semanal se especifica mediante el elemento [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="ec7de-114">When reading or writing your own XML for a task, the interval for a weekly schedule is specified using the [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec7de-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec7de-115">Requirements</span></span>



| <span data-ttu-id="ec7de-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec7de-116">Requirement</span></span> | <span data-ttu-id="ec7de-117">Value</span><span class="sxs-lookup"><span data-stu-id="ec7de-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7de-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec7de-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ec7de-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ec7de-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ec7de-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec7de-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ec7de-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ec7de-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ec7de-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ec7de-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec7de-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ec7de-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ec7de-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ec7de-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec7de-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec7de-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec7de-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec7de-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec7de-127">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ec7de-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





