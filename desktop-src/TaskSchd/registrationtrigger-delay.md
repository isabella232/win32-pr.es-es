---
title: RegistrationTrigger. Delay (propiedad)
description: En el caso de scripting, obtiene o establece la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea.
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- Propiedad Delay Programador de tareas
- Propiedad Delay Programador de tareas, objeto RegistrationTrigger
- Programador de tareas de objeto RegistrationTrigger, propiedad Delay
topic_type:
- apiref
api_name:
- RegistrationTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad86017547ac4476f430e13e2566ddd6d3494226
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534989"
---
# <a name="registrationtriggerdelay-property"></a><span data-ttu-id="e0fa1-106">RegistrationTrigger. Delay (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e0fa1-106">RegistrationTrigger.Delay property</span></span>

<span data-ttu-id="e0fa1-107">En el caso de scripting, obtiene o establece la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="e0fa1-107">For scripting, gets or sets the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="e0fa1-108">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="e0fa1-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0fa1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0fa1-109">Syntax</span></span>


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="e0fa1-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e0fa1-110">Property value</span></span>

<span data-ttu-id="e0fa1-111">La cantidad de tiempo entre el momento en que se registra el sistema y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="e0fa1-111">The amount of time between when the system is registered and when the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0fa1-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0fa1-112">Remarks</span></span>

<span data-ttu-id="e0fa1-113">Al leer o escribir XML para una tarea, el retraso de arranque se especifica mediante el elemento [**Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="e0fa1-113">When reading or writing XML for a task, the boot delay is specified using the [**Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="e0fa1-114">Si se registra una tarea con un desencadenador de registro retrasado y el equipo en el que se ha registrado la tarea se cierra o se reinicia durante el retraso, antes de que se ejecute la tarea, la tarea no se ejecutará y se perderá el retraso.</span><span class="sxs-lookup"><span data-stu-id="e0fa1-114">If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during the delay, before the task runs, then the task will not run and the delay will be lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0fa1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0fa1-115">Requirements</span></span>



| <span data-ttu-id="e0fa1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0fa1-116">Requirement</span></span> | <span data-ttu-id="e0fa1-117">Value</span><span class="sxs-lookup"><span data-stu-id="e0fa1-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0fa1-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0fa1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e0fa1-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e0fa1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e0fa1-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0fa1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e0fa1-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e0fa1-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e0fa1-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e0fa1-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="e0fa1-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e0fa1-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e0fa1-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e0fa1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0fa1-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0fa1-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0fa1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0fa1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0fa1-127">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="e0fa1-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





