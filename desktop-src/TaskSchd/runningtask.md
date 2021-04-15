---
title: Objeto RunningTask
description: Objeto de scripting que proporciona los métodos para obtener información y controlar una tarea en ejecución.
ms.assetid: 335e69d8-affa-4845-a067-641184e0f7df
keywords:
- Objeto RunningTask Programador de tareas
- Programador de tareas de objeto RunningTask, descrito
topic_type:
- apiref
api_name:
- RunningTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261be07f71d0d35f5d3140de1b39574b635a531e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534594"
---
# <a name="runningtask-object"></a><span data-ttu-id="4c51d-105">Objeto RunningTask</span><span class="sxs-lookup"><span data-stu-id="4c51d-105">RunningTask object</span></span>

<span data-ttu-id="4c51d-106">Objeto de scripting que proporciona los métodos para obtener información y controlar una tarea en ejecución.</span><span class="sxs-lookup"><span data-stu-id="4c51d-106">Scripting object that provides the methods to get information from and control a running task.</span></span>

## <a name="members"></a><span data-ttu-id="4c51d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4c51d-107">Members</span></span>

<span data-ttu-id="4c51d-108">El objeto **RunningTask** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4c51d-108">The **RunningTask** object has these types of members:</span></span>

-   [<span data-ttu-id="4c51d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="4c51d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="4c51d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4c51d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4c51d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4c51d-111">Methods</span></span>

<span data-ttu-id="4c51d-112">El objeto **RunningTask** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4c51d-112">The **RunningTask** object has these methods.</span></span>



| <span data-ttu-id="4c51d-113">Método</span><span class="sxs-lookup"><span data-stu-id="4c51d-113">Method</span></span>                                 | <span data-ttu-id="4c51d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c51d-114">Description</span></span>                                                           |
|:---------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="4c51d-115">**Actualizar**</span><span class="sxs-lookup"><span data-stu-id="4c51d-115">**Refresh**</span></span>](runningtask-refresh.md) | <span data-ttu-id="4c51d-116">Actualiza todas las variables de instancia local de la tarea.</span><span class="sxs-lookup"><span data-stu-id="4c51d-116">Refreshes all of the local instance variables of the task.</span></span><br/> |
| [<span data-ttu-id="4c51d-117">**Stop**</span><span class="sxs-lookup"><span data-stu-id="4c51d-117">**Stop**</span></span>](runningtask-stop.md)       | <span data-ttu-id="4c51d-118">Detiene esta instancia de la tarea.</span><span class="sxs-lookup"><span data-stu-id="4c51d-118">Stops this instance of the task.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="4c51d-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4c51d-119">Properties</span></span>

<span data-ttu-id="4c51d-120">El objeto **RunningTask** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4c51d-120">The **RunningTask** object has these properties.</span></span>



| <span data-ttu-id="4c51d-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4c51d-121">Property</span></span>                                                      | <span data-ttu-id="4c51d-122">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="4c51d-122">Access type</span></span>          | <span data-ttu-id="4c51d-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c51d-123">Description</span></span>                                                                         |
|:--------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c51d-124">**CurrentAction**</span><span class="sxs-lookup"><span data-stu-id="4c51d-124">**CurrentAction**</span></span>](runningtask-currentaction.md)<br/> | <span data-ttu-id="4c51d-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c51d-125">Read-only</span></span><br/> | <span data-ttu-id="4c51d-126">Obtiene el nombre de la acción actual que está realizando la tarea en ejecución.</span><span class="sxs-lookup"><span data-stu-id="4c51d-126">Gets the name of the current action that the running task is performing.</span></span><br/> |
| [<span data-ttu-id="4c51d-127">**EnginePID**</span><span class="sxs-lookup"><span data-stu-id="4c51d-127">**EnginePID**</span></span>](runningtask-enginepid.md)<br/>         | <span data-ttu-id="4c51d-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c51d-128">Read-only</span></span><br/> | <span data-ttu-id="4c51d-129">Obtiene el identificador de proceso del motor (proceso) que está ejecutando la tarea.</span><span class="sxs-lookup"><span data-stu-id="4c51d-129">Gets the process ID for the engine (process) which is running the task.</span></span><br/>  |
| [<span data-ttu-id="4c51d-130">**Valor FileStream**</span><span class="sxs-lookup"><span data-stu-id="4c51d-130">**InstanceGuid**</span></span>](runningtask-instanceguid.md)<br/>   | <span data-ttu-id="4c51d-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c51d-131">Read-only</span></span><br/> | <span data-ttu-id="4c51d-132">Obtiene el identificador GUID para esta instancia de la tarea.</span><span class="sxs-lookup"><span data-stu-id="4c51d-132">Gets the GUID identifier for this instance of the task.</span></span><br/>                  |
| [<span data-ttu-id="4c51d-133">**Name**</span><span class="sxs-lookup"><span data-stu-id="4c51d-133">**Name**</span></span>](runningtask-name.md)<br/>                   | <span data-ttu-id="4c51d-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c51d-134">Read-only</span></span><br/> | <span data-ttu-id="4c51d-135">Obtiene el nombre de la tarea.</span><span class="sxs-lookup"><span data-stu-id="4c51d-135">Gets the name of the task.</span></span><br/>                                               |
| [<span data-ttu-id="4c51d-136">**Ruta**</span><span class="sxs-lookup"><span data-stu-id="4c51d-136">**Path**</span></span>](runningtask-path.md)<br/>                   | <span data-ttu-id="4c51d-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c51d-137">Read-only</span></span><br/> | <span data-ttu-id="4c51d-138">Obtiene la ruta de acceso donde se almacena la tarea.</span><span class="sxs-lookup"><span data-stu-id="4c51d-138">Gets the path to where the task is stored.</span></span><br/>                               |
| [<span data-ttu-id="4c51d-139">**State**</span><span class="sxs-lookup"><span data-stu-id="4c51d-139">**State**</span></span>](runningtask-state.md)<br/>                 | <span data-ttu-id="4c51d-140">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c51d-140">Read-only</span></span><br/> | <span data-ttu-id="4c51d-141">Obtiene el estado de la tarea en ejecución.</span><span class="sxs-lookup"><span data-stu-id="4c51d-141">Gets the state of the running task.</span></span> <br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="4c51d-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c51d-142">Requirements</span></span>



| <span data-ttu-id="4c51d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c51d-143">Requirement</span></span> | <span data-ttu-id="4c51d-144">Value</span><span class="sxs-lookup"><span data-stu-id="4c51d-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c51d-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c51d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="4c51d-146">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4c51d-146">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4c51d-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c51d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="4c51d-148">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4c51d-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4c51d-149">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4c51d-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="4c51d-150"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4c51d-150"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4c51d-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4c51d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c51d-152"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c51d-152"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c51d-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c51d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c51d-154">Objetos Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="4c51d-154">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="4c51d-155">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="4c51d-155">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="4c51d-156">**RunningTaskCollection**</span><span class="sxs-lookup"><span data-stu-id="4c51d-156">**RunningTaskCollection**</span></span>](runningtaskcollection.md)
</dt> <dt>

[<span data-ttu-id="4c51d-157">**RegisteredTask. Run**</span><span class="sxs-lookup"><span data-stu-id="4c51d-157">**RegisteredTask.Run**</span></span>](registeredtask-run.md)
</dt> <dt>

[<span data-ttu-id="4c51d-158">**RegisteredTask.RunEx**</span><span class="sxs-lookup"><span data-stu-id="4c51d-158">**RegisteredTask.RunEx**</span></span>](registeredtask-runex.md)
</dt> </dl>

 

 





