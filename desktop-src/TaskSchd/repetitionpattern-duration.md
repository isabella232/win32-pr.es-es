---
title: RepetitionPattern. Duration (propiedad)
description: En el caso de scripting, obtiene o establece el tiempo que se repite el patrón.
ms.assetid: 41a56414-981b-440a-b51a-228125baf303
keywords:
- Propiedad duration Programador de tareas
- Propiedad duration Programador de tareas, objeto RepetitionPattern
- Programador de tareas de objeto RepetitionPattern, propiedad duration
topic_type:
- apiref
api_name:
- RepetitionPattern.Duration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ff18330fd69bb54fdfb489b72f9470f707aed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686084"
---
# <a name="repetitionpatternduration-property"></a><span data-ttu-id="30fe2-106">RepetitionPattern. Duration (propiedad)</span><span class="sxs-lookup"><span data-stu-id="30fe2-106">RepetitionPattern.Duration property</span></span>

<span data-ttu-id="30fe2-107">En el caso de scripting, obtiene o establece el tiempo que se repite el patrón.</span><span class="sxs-lookup"><span data-stu-id="30fe2-107">For scripting, gets or sets how long the pattern is repeated.</span></span>

## <a name="syntax"></a><span data-ttu-id="30fe2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30fe2-108">Syntax</span></span>


```VB
RepetitionPattern.Duration As String
```



## <a name="property-value"></a><span data-ttu-id="30fe2-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="30fe2-109">Property value</span></span>

<span data-ttu-id="30fe2-110">Cuánto tiempo se repite el patrón.</span><span class="sxs-lookup"><span data-stu-id="30fe2-110">How long the pattern is repeated.</span></span> <span data-ttu-id="30fe2-111">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="30fe2-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="30fe2-112">El tiempo mínimo permitido es de un minuto.</span><span class="sxs-lookup"><span data-stu-id="30fe2-112">The minimum time allowed is one minute.</span></span>

<span data-ttu-id="30fe2-113">Si no se especifica ningún valor para la duración, el patrón se repite indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="30fe2-113">If no value is specified for the duration, then the pattern is repeated indefinitely.</span></span>

## <a name="remarks"></a><span data-ttu-id="30fe2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30fe2-114">Remarks</span></span>

<span data-ttu-id="30fe2-115">Si especifica una duración de repetición para una tarea, también debe especificar el intervalo de repetición.</span><span class="sxs-lookup"><span data-stu-id="30fe2-115">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="30fe2-116">Al leer o escribir XML para una tarea, la duración de repetición se especifica en el elemento [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="30fe2-116">When reading or writing XML for a task, the repetition duration is specified in the [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="30fe2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30fe2-117">Requirements</span></span>



| <span data-ttu-id="30fe2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="30fe2-118">Requirement</span></span> | <span data-ttu-id="30fe2-119">Value</span><span class="sxs-lookup"><span data-stu-id="30fe2-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30fe2-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30fe2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30fe2-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="30fe2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="30fe2-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30fe2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30fe2-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="30fe2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30fe2-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="30fe2-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="30fe2-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="30fe2-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="30fe2-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="30fe2-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30fe2-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30fe2-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30fe2-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="30fe2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30fe2-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="30fe2-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





