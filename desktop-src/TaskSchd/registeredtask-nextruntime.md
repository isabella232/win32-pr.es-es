---
title: Propiedad RegisteredTask. NextRunTime
description: En el caso de scripting, obtiene la hora a la que se programa la próxima ejecución de la tarea registrada.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- Programador de tareas de la propiedad NextRunTime
- Programador de tareas de la propiedad NextRunTime, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, propiedad NextRunTime
topic_type:
- apiref
api_name:
- RegisteredTask.NextRunTime
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94db26c023ddd2c146586fbc433548517a84f234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803235"
---
# <a name="registeredtasknextruntime-property"></a><span data-ttu-id="f1e85-106">Propiedad RegisteredTask. NextRunTime</span><span class="sxs-lookup"><span data-stu-id="f1e85-106">RegisteredTask.NextRunTime property</span></span>

<span data-ttu-id="f1e85-107">En el caso de scripting, obtiene la hora a la que se programa la próxima ejecución de la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="f1e85-107">For scripting, gets the time when the registered task is next scheduled to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1e85-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1e85-108">Syntax</span></span>


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a><span data-ttu-id="f1e85-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f1e85-109">Property value</span></span>

<span data-ttu-id="f1e85-110">La hora a la que se ha programado la próxima ejecución de la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="f1e85-110">The time when the registered task is next scheduled to run.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1e85-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1e85-111">Remarks</span></span>

<span data-ttu-id="f1e85-112">Si la tarea registrada contiene desencadenadores que se deshabilitan de forma individual, estos desencadenadores todavía afectarán a la siguiente hora de ejecución programada que se devuelva aunque estén deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="f1e85-112">If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1e85-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1e85-113">Requirements</span></span>



| <span data-ttu-id="f1e85-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1e85-114">Requirement</span></span> | <span data-ttu-id="f1e85-115">Value</span><span class="sxs-lookup"><span data-stu-id="f1e85-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e85-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1e85-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f1e85-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f1e85-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f1e85-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1e85-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f1e85-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f1e85-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f1e85-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f1e85-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="f1e85-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f1e85-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f1e85-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f1e85-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1e85-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1e85-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1e85-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1e85-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e85-125">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f1e85-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="f1e85-126">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="f1e85-126">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





