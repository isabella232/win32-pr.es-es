---
title: Propiedad RegisteredTask. State
description: En el caso de scripting, obtiene el estado operativo de la tarea registrada.
ms.assetid: 1acd4946-322f-4f24-b317-92be80e19de5
keywords:
- Programador de tareas de propiedad de estado
- Propiedad State Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, propiedad State
topic_type:
- apiref
api_name:
- RegisteredTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47af082174bc6927a16760e87566f311ec9f4a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492802"
---
# <a name="registeredtaskstate-property"></a><span data-ttu-id="d9dd9-106">Propiedad RegisteredTask. State</span><span class="sxs-lookup"><span data-stu-id="d9dd9-106">RegisteredTask.State property</span></span>

<span data-ttu-id="d9dd9-107">En el caso de scripting, obtiene el estado operativo de la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="d9dd9-107">For scripting, gets the operational state of the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9dd9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9dd9-108">Syntax</span></span>


```VB
RegisteredTask.State As Integer
```



## <a name="property-value"></a><span data-ttu-id="d9dd9-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d9dd9-109">Property value</span></span>

<span data-ttu-id="d9dd9-110">Constante [**de \_ Estado de tarea**](/windows/desktop/api/taskschd/ne-taskschd-task_state) que define el estado operativo de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d9dd9-110">A [**TASK\_STATE**](/windows/desktop/api/taskschd/ne-taskschd-task_state) constant that defines the operational state of the task.</span></span>



| <span data-ttu-id="d9dd9-111">Value</span><span class="sxs-lookup"><span data-stu-id="d9dd9-111">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="d9dd9-112">Significado</span><span class="sxs-lookup"><span data-stu-id="d9dd9-112">Meaning</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <span data-ttu-id="d9dd9-113"><dt>**Tarea \_ de ESTADO \_ desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d9dd9-113"><dt>**TASK\_STATE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="d9dd9-114">No se conoce el estado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d9dd9-114">The state of the task is unknown.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <span data-ttu-id="d9dd9-115"><dt>**Tarea \_ de ESTADO \_ deshabilitado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d9dd9-115"><dt>**TASK\_STATE\_DISABLED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="d9dd9-116">La tarea está registrada, pero está deshabilitada y ninguna instancia de la tarea está en cola o en ejecución.</span><span class="sxs-lookup"><span data-stu-id="d9dd9-116">The task is registered but is disabled and no instances of the task are queued or running.</span></span> <span data-ttu-id="d9dd9-117">La tarea no se puede ejecutar hasta que se habilite.</span><span class="sxs-lookup"><span data-stu-id="d9dd9-117">The task cannot be run until it is enabled.</span></span><br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <span data-ttu-id="d9dd9-118"><dt>**Tarea \_ de ESTADO \_ en cola**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d9dd9-118"><dt>**TASK\_STATE\_QUEUED**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="d9dd9-119">Las instancias de la tarea se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="d9dd9-119">Instances of the task are queued.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <span data-ttu-id="d9dd9-120"><dt>**Tarea \_ de ESTADO \_ preparado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d9dd9-120"><dt>**TASK\_STATE\_READY**</dt> <dt>3</dt></span></span> </dl>          | <span data-ttu-id="d9dd9-121">La tarea está lista para ejecutarse, pero no hay ninguna instancia en cola o en ejecución.</span><span class="sxs-lookup"><span data-stu-id="d9dd9-121">The task is ready to be executed, but no instances are queued or running.</span></span><br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <span data-ttu-id="d9dd9-122"><dt>**Tarea \_ de Estado en \_ ejecución**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d9dd9-122"><dt>**TASK\_STATE\_RUNNING**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="d9dd9-123">Se están ejecutando una o varias instancias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d9dd9-123">One or more instances of the task are running.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="d9dd9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9dd9-124">Requirements</span></span>



| <span data-ttu-id="d9dd9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9dd9-125">Requirement</span></span> | <span data-ttu-id="d9dd9-126">Value</span><span class="sxs-lookup"><span data-stu-id="d9dd9-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9dd9-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9dd9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d9dd9-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d9dd9-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d9dd9-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9dd9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d9dd9-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9dd9-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d9dd9-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d9dd9-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="d9dd9-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d9dd9-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d9dd9-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9dd9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9dd9-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9dd9-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9dd9-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9dd9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9dd9-136">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="d9dd9-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d9dd9-137">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="d9dd9-137">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





