---
title: Propiedad RunningTask. State
description: En el caso de scripting, obtiene un identificador para el estado de la tarea en ejecución.
ms.assetid: 048863f4-b80b-42ab-bd74-ec761a8f03aa
keywords:
- Programador de tareas de propiedad de estado
- Propiedad State Programador de tareas, objeto RunningTask
- Programador de tareas de objeto RunningTask, propiedad State
topic_type:
- apiref
api_name:
- RunningTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b962de116eef1301be209828181147dfe03273e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801790"
---
# <a name="runningtaskstate-property"></a><span data-ttu-id="cbf41-106">Propiedad RunningTask. State</span><span class="sxs-lookup"><span data-stu-id="cbf41-106">RunningTask.State property</span></span>

<span data-ttu-id="cbf41-107">En el caso de scripting, obtiene un identificador para el estado de la tarea en ejecución.</span><span class="sxs-lookup"><span data-stu-id="cbf41-107">For scripting, gets an identifier for the state of the running task.</span></span>

<span data-ttu-id="cbf41-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cbf41-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbf41-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbf41-109">Syntax</span></span>


```VB
RunningTask.State As String
```



## <a name="property-value"></a><span data-ttu-id="cbf41-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="cbf41-110">Property value</span></span>

<span data-ttu-id="cbf41-111">Identificador del estado de la tarea en ejecución.</span><span class="sxs-lookup"><span data-stu-id="cbf41-111">An identifier for the state of the running task.</span></span>



| <span data-ttu-id="cbf41-112">Value</span><span class="sxs-lookup"><span data-stu-id="cbf41-112">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="cbf41-113">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf41-113">Meaning</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <span data-ttu-id="cbf41-114"><dt>**Tarea \_ de ESTADO \_ desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cbf41-114"><dt>**TASK\_STATE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="cbf41-115">No se conoce el estado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="cbf41-115">The state of the task is unknown.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <span data-ttu-id="cbf41-116"><dt>**Tarea \_ de ESTADO \_ deshabilitado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cbf41-116"><dt>**TASK\_STATE\_DISABLED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="cbf41-117">La tarea está registrada, pero está deshabilitada y ninguna instancia de la tarea está en cola o en ejecución.</span><span class="sxs-lookup"><span data-stu-id="cbf41-117">The task is registered but is disabled and no instances of the task are queued or running.</span></span> <span data-ttu-id="cbf41-118">La tarea no se puede ejecutar hasta que se habilite.</span><span class="sxs-lookup"><span data-stu-id="cbf41-118">The task cannot be run until it is enabled.</span></span><br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <span data-ttu-id="cbf41-119"><dt>**Tarea \_ de ESTADO \_ en cola**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="cbf41-119"><dt>**TASK\_STATE\_QUEUED**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="cbf41-120">Las instancias de la tarea se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="cbf41-120">Instances of the task are queued.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <span data-ttu-id="cbf41-121"><dt>**Tarea \_ de ESTADO \_ preparado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="cbf41-121"><dt>**TASK\_STATE\_READY**</dt> <dt>3</dt></span></span> </dl>          | <span data-ttu-id="cbf41-122">La tarea está lista para ejecutarse, pero no hay ninguna instancia en cola o en ejecución.</span><span class="sxs-lookup"><span data-stu-id="cbf41-122">The task is ready to be executed, but no instances are queued or running.</span></span><br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <span data-ttu-id="cbf41-123"><dt>**Tarea \_ de Estado en \_ ejecución**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="cbf41-123"><dt>**TASK\_STATE\_RUNNING**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="cbf41-124">Se están ejecutando una o varias instancias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="cbf41-124">One or more instances of the task are running.</span></span><br/>                                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="cbf41-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cbf41-125">Remarks</span></span>

<span data-ttu-id="cbf41-126">Se llama al método [**RunningTask. Refresh**](runningtask-refresh.md) antes de que se devuelva el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf41-126">The [**RunningTask.Refresh**](runningtask-refresh.md) method is called before the property value is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbf41-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbf41-127">Requirements</span></span>



| <span data-ttu-id="cbf41-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbf41-128">Requirement</span></span> | <span data-ttu-id="cbf41-129">Value</span><span class="sxs-lookup"><span data-stu-id="cbf41-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf41-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbf41-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cbf41-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cbf41-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cbf41-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbf41-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cbf41-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cbf41-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cbf41-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cbf41-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="cbf41-135"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cbf41-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cbf41-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cbf41-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbf41-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbf41-137"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





