---
title: Trigger. repite (propiedad)
description: Para scripting, obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- Programador de tareas de propiedad de repetición
- Propiedad repite Programador de tareas, objeto desencadenador
- Objeto desencadenador Programador de tareas, propiedad repite
topic_type:
- apiref
api_name:
- Trigger.Repetition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611c7e42a14de06a8777333a6dc640781943ba06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676679"
---
# <a name="triggerrepetition-property"></a><span data-ttu-id="a1f3a-106">Trigger. repite (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a1f3a-106">Trigger.Repetition property</span></span>

<span data-ttu-id="a1f3a-107">Para scripting, obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="a1f3a-107">For scripting, gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f3a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1f3a-108">Syntax</span></span>


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a><span data-ttu-id="a1f3a-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a1f3a-109">Property value</span></span>

<span data-ttu-id="a1f3a-110">Un objeto [**RepetitionPattern**](repetitionpattern.md) que define la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="a1f3a-110">A [**RepetitionPattern**](repetitionpattern.md) object that defines how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1f3a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1f3a-111">Remarks</span></span>

<span data-ttu-id="a1f3a-112">Al leer o escribir su propio XML para una tarea, el patrón de repetición de un desencadenador se especifica en el elemento [**repite**](taskschedulerschema-repetition-triggerbasetype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="a1f3a-112">When reading or writing your own XML for a task, the repetition pattern for a trigger is specified in the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1f3a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1f3a-113">Requirements</span></span>



| <span data-ttu-id="a1f3a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1f3a-114">Requirement</span></span> | <span data-ttu-id="a1f3a-115">Value</span><span class="sxs-lookup"><span data-stu-id="a1f3a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1f3a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1f3a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a1f3a-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a1f3a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a1f3a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1f3a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a1f3a-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1f3a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a1f3a-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a1f3a-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="a1f3a-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a1f3a-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a1f3a-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a1f3a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1f3a-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1f3a-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1f3a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1f3a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f3a-125">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="a1f3a-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="a1f3a-126">**RepetitionPattern**</span><span class="sxs-lookup"><span data-stu-id="a1f3a-126">**RepetitionPattern**</span></span>](repetitionpattern.md)
</dt> </dl>

 

 





