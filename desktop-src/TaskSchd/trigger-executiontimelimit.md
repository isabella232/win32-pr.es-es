---
title: Trigger.Exepropiedad cutionTimeLimit
description: En el caso de scripting, obtiene o establece la cantidad máxima de tiempo que puede ejecutarse la tarea iniciada por el desencadenador.
ms.assetid: 9993b362-f8f7-429b-a16a-1845d6f0f5e0
keywords:
- Programador de tareas de la propiedad ExecutionTimeLimit
- Propiedad ExecutionTimeLimit Programador de tareas, objeto desencadenador
- Programador de tareas de objeto desencadenador, propiedad ExecutionTimeLimit
topic_type:
- apiref
api_name:
- Trigger.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974a9adebf8ca29fe8626c938c37580d0628771b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996151"
---
# <a name="triggerexecutiontimelimit-property"></a><span data-ttu-id="153dd-106">Trigger.Exepropiedad cutionTimeLimit</span><span class="sxs-lookup"><span data-stu-id="153dd-106">Trigger.ExecutionTimeLimit property</span></span>

<span data-ttu-id="153dd-107">En el caso de scripting, obtiene o establece la cantidad máxima de tiempo que puede ejecutarse la tarea iniciada por el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="153dd-107">For scripting, gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="153dd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="153dd-108">Syntax</span></span>


```VB
Trigger.ExecutionTimeLimit As String
```



## <a name="property-value"></a><span data-ttu-id="153dd-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="153dd-109">Property value</span></span>

<span data-ttu-id="153dd-110">Cantidad máxima de tiempo que se permite la ejecución de la tarea iniciada por el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="153dd-110">The maximum amount of time that the task launched by the trigger is allowed to run.</span></span> <span data-ttu-id="153dd-111">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="153dd-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="153dd-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="153dd-112">Remarks</span></span>

<span data-ttu-id="153dd-113">Al leer o escribir XML para una tarea, el límite de tiempo de ejecución se especifica en el elemento [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="153dd-113">When reading or writing XML for a task, the execution time limit is specified in the [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="153dd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="153dd-114">Requirements</span></span>



| <span data-ttu-id="153dd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="153dd-115">Requirement</span></span> | <span data-ttu-id="153dd-116">Value</span><span class="sxs-lookup"><span data-stu-id="153dd-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="153dd-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="153dd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="153dd-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="153dd-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="153dd-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="153dd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="153dd-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="153dd-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="153dd-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="153dd-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="153dd-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="153dd-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="153dd-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="153dd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="153dd-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="153dd-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="153dd-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="153dd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="153dd-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="153dd-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





