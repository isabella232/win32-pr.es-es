---
title: Propiedad RepetitionPattern.Interval
description: Para el scripting, obtiene o establece la cantidad de tiempo entre cada reinicio de la tarea.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Intervalo de propiedades Programador de tareas
- Propiedad Interval Programador de tareas , objeto RepetitionPattern
- Objeto RepetitionPattern Programador de tareas , propiedad Interval
topic_type:
- apiref
api_name:
- RepetitionPattern.Interval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e81920fffe5c9fd58dd36a028b924f54ebe6dd
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734180"
---
# <a name="repetitionpatterninterval-property"></a><span data-ttu-id="d996b-106">Propiedad RepetitionPattern.Interval</span><span class="sxs-lookup"><span data-stu-id="d996b-106">RepetitionPattern.Interval property</span></span>

<span data-ttu-id="d996b-107">Para el scripting, obtiene o establece la cantidad de tiempo entre cada reinicio de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d996b-107">For scripting, gets or sets the amount of time between each restart of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="d996b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d996b-108">Syntax</span></span>


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a><span data-ttu-id="d996b-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d996b-109">Property value</span></span>

<span data-ttu-id="d996b-110">Cantidad de tiempo entre cada reinicio de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d996b-110">The amount of time between each restart of the task.</span></span> <span data-ttu-id="d996b-111">El formato de esta cadena es `P<days>DT<hours>H<minutes>M<seconds>S` (por ejemplo, "PT5M" es 5 minutos, "PT1H" es 1 hora y "PT20M" es 20 minutos).</span><span class="sxs-lookup"><span data-stu-id="d996b-111">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="d996b-112">El tiempo máximo permitido es de 31 días y el tiempo mínimo permitido es de 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="d996b-112">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="d996b-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d996b-113">Remarks</span></span>

<span data-ttu-id="d996b-114">Si especifica una duración de repetición para una tarea, también debe especificar el intervalo de repetición.</span><span class="sxs-lookup"><span data-stu-id="d996b-114">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="d996b-115">Al leer o escribir XML para una tarea, el intervalo de repetición se especifica en el [**elemento Interval**](taskschedulerschema-interval-repetitiontype-element.md) del Programador de tareas esquema.</span><span class="sxs-lookup"><span data-stu-id="d996b-115">When reading or writing XML for a task, the repetition interval is specified in the [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d996b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d996b-116">Requirements</span></span>



| <span data-ttu-id="d996b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d996b-117">Requirement</span></span> | <span data-ttu-id="d996b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d996b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d996b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d996b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d996b-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d996b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d996b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d996b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d996b-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d996b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d996b-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d996b-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="d996b-124"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d996b-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d996b-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d996b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d996b-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d996b-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d996b-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d996b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d996b-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="d996b-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





