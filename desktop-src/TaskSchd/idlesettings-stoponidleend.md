---
title: Propiedad IdleSettings. StopOnIdleEnd
description: Para scripting, obtiene o establece un valor booleano que indica que el Programador de tareas finalizará la tarea si la condición de inactividad finaliza antes de que se complete la tarea.
ms.assetid: 5908bf6b-227a-4234-a741-82cf38163171
keywords:
- Programador de tareas de la propiedad StopOnIdleEnd
- Programador de tareas de la propiedad StopOnIdleEnd, objeto IdleSettings
- Programador de tareas de objeto IdleSettings, propiedad StopOnIdleEnd
topic_type:
- apiref
api_name:
- IdleSettings.StopOnIdleEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f475c0a05d43cf0fbdd7097c1ee083f9040b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905090"
---
# <a name="idlesettingsstoponidleend-property"></a><span data-ttu-id="d88fe-106">Propiedad IdleSettings. StopOnIdleEnd</span><span class="sxs-lookup"><span data-stu-id="d88fe-106">IdleSettings.StopOnIdleEnd property</span></span>

<span data-ttu-id="d88fe-107">Para scripting, obtiene o establece un valor booleano que indica que el Programador de tareas finalizará la tarea si la condición de inactividad finaliza antes de que se complete la tarea.</span><span class="sxs-lookup"><span data-stu-id="d88fe-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d88fe-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d88fe-108">Syntax</span></span>


```VB
IdleSettings.StopOnIdleEnd As Boolean
```



## <a name="property-value"></a><span data-ttu-id="d88fe-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d88fe-109">Property value</span></span>

<span data-ttu-id="d88fe-110">Un valor booleano que indica que el Programador de tareas finalizará la tarea si la condición de inactividad finaliza antes de que se complete la tarea.</span><span class="sxs-lookup"><span data-stu-id="d88fe-110">A Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d88fe-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d88fe-111">Remarks</span></span>

<span data-ttu-id="d88fe-112">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="d88fe-112">When reading or writing XML for a task, this setting is specified in the [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d88fe-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d88fe-113">Requirements</span></span>



| <span data-ttu-id="d88fe-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d88fe-114">Requirement</span></span> | <span data-ttu-id="d88fe-115">Value</span><span class="sxs-lookup"><span data-stu-id="d88fe-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d88fe-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d88fe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d88fe-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d88fe-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d88fe-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d88fe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d88fe-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d88fe-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d88fe-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d88fe-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="d88fe-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d88fe-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d88fe-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d88fe-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d88fe-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d88fe-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d88fe-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d88fe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d88fe-125">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="d88fe-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d88fe-126">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="d88fe-126">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





