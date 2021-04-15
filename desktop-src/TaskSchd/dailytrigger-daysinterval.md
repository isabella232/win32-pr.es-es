---
title: Propiedad DailyTrigger. DaysInterval
description: En el caso de scripting, obtiene o establece el intervalo entre los días de la programación.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- Programador de tareas de la propiedad DaysInterval
- Programador de tareas de la propiedad DaysInterval, objeto DailyTrigger
- Programador de tareas de objeto DailyTrigger, propiedad DaysInterval
topic_type:
- apiref
api_name:
- DailyTrigger.DaysInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6499f3b900fe10b2a2527c2e2ee675cca3151204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534300"
---
# <a name="dailytriggerdaysinterval-property"></a><span data-ttu-id="943d2-106">Propiedad DailyTrigger. DaysInterval</span><span class="sxs-lookup"><span data-stu-id="943d2-106">DailyTrigger.DaysInterval property</span></span>

<span data-ttu-id="943d2-107">En el caso de scripting, obtiene o establece el intervalo entre los días de la programación.</span><span class="sxs-lookup"><span data-stu-id="943d2-107">For scripting, gets or sets the interval between the days in the schedule.</span></span>

## <a name="syntax"></a><span data-ttu-id="943d2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="943d2-108">Syntax</span></span>


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a><span data-ttu-id="943d2-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="943d2-109">Property value</span></span>

<span data-ttu-id="943d2-110">Intervalo entre los días de la programación.</span><span class="sxs-lookup"><span data-stu-id="943d2-110">The interval between the days in the schedule.</span></span>

## <a name="remarks"></a><span data-ttu-id="943d2-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="943d2-111">Remarks</span></span>

<span data-ttu-id="943d2-112">Un intervalo de 1 genera una programación diaria.</span><span class="sxs-lookup"><span data-stu-id="943d2-112">An interval of 1 produces a daily schedule.</span></span> <span data-ttu-id="943d2-113">Un intervalo de 2 genera una programación de todos los días.</span><span class="sxs-lookup"><span data-stu-id="943d2-113">An interval of 2 produces an every-other day schedule.</span></span>

<span data-ttu-id="943d2-114">Al leer o escribir su propio XML para una tarea, el intervalo de una programación diaria se especifica mediante el elemento [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="943d2-114">When reading or writing your own XML for a task, the interval for a daily schedule is specified using the [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="943d2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="943d2-115">Requirements</span></span>



| <span data-ttu-id="943d2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="943d2-116">Requirement</span></span> | <span data-ttu-id="943d2-117">Value</span><span class="sxs-lookup"><span data-stu-id="943d2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="943d2-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="943d2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="943d2-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="943d2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="943d2-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="943d2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="943d2-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="943d2-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="943d2-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="943d2-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="943d2-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="943d2-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="943d2-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="943d2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="943d2-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="943d2-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="943d2-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="943d2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="943d2-127">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="943d2-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="943d2-128">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="943d2-128">**DailyTrigger**</span></span>](dailytrigger.md)
</dt> </dl>

 

 





