---
title: EventTrigger. Delay (propiedad)
description: En el caso de scripting, obtiene o establece un valor que indica la cantidad de tiempo entre el momento en que se produce el evento y el momento en que se inicia la tarea.
ms.assetid: 6f8b5e25-ad53-466e-adab-fe3c968e941b
keywords:
- Propiedad Delay Programador de tareas
- Propiedad Delay Programador de tareas, objeto EventTrigger
- Objeto EventTrigger Programador de tareas, propiedad Delay
topic_type:
- apiref
api_name:
- EventTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb67ca7ef12ca023bcb6c0d9d83880d4abb94af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676779"
---
# <a name="eventtriggerdelay-property"></a><span data-ttu-id="f1ee0-106">EventTrigger. Delay (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f1ee0-106">EventTrigger.Delay property</span></span>

<span data-ttu-id="f1ee0-107">En el caso de scripting, obtiene o establece un valor que indica la cantidad de tiempo entre el momento en que se produce el evento y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="f1ee0-107">For scripting, gets or sets a value that indicates the amount of time between when the event occurs and when the task is started.</span></span> <span data-ttu-id="f1ee0-108">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="f1ee0-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ee0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1ee0-109">Syntax</span></span>


```VB
EventTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="f1ee0-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f1ee0-110">Property value</span></span>

<span data-ttu-id="f1ee0-111">Valor que indica la cantidad de tiempo entre el momento en que se produce el evento y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="f1ee0-111">A value that indicates the amount of time between when the event occurs and when the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1ee0-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1ee0-112">Remarks</span></span>

<span data-ttu-id="f1ee0-113">Al leer o escribir su propio XML para una tarea, el retraso del evento se especifica mediante el elemento [**Delay**](taskschedulerschema-delay-eventtriggertype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="f1ee0-113">When reading or writing your own XML for a task, the event delay is specified using the [**Delay**](taskschedulerschema-delay-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1ee0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1ee0-114">Requirements</span></span>



| <span data-ttu-id="f1ee0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1ee0-115">Requirement</span></span> | <span data-ttu-id="f1ee0-116">Value</span><span class="sxs-lookup"><span data-stu-id="f1ee0-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ee0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1ee0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f1ee0-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f1ee0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f1ee0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1ee0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f1ee0-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f1ee0-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f1ee0-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f1ee0-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="f1ee0-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f1ee0-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f1ee0-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f1ee0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1ee0-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1ee0-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1ee0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1ee0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1ee0-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f1ee0-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="f1ee0-127">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="f1ee0-127">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

 





