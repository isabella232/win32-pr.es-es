---
title: Objeto RegisteredTask
description: Objeto de scripting que proporciona los métodos que se usan para ejecutar la tarea inmediatamente, obtener las instancias en ejecución de la tarea, obtener o establecer las credenciales que se usan para registrar la tarea y las propiedades que describen la tarea.
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- Objeto RegisteredTask Programador de tareas
- Programador de tareas de objeto RegisteredTask, descrito
topic_type:
- apiref
api_name:
- RegisteredTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ce300375e5122a7b63266c0cd21cdddf34606b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801502"
---
# <a name="registeredtask-object"></a><span data-ttu-id="7b804-105">Objeto RegisteredTask</span><span class="sxs-lookup"><span data-stu-id="7b804-105">RegisteredTask object</span></span>

<span data-ttu-id="7b804-106">Objeto de scripting que proporciona los métodos que se usan para ejecutar la tarea inmediatamente, obtener las instancias en ejecución de la tarea, obtener o establecer las credenciales que se usan para registrar la tarea y las propiedades que describen la tarea.</span><span class="sxs-lookup"><span data-stu-id="7b804-106">Scripting object that provides the methods that are used to run the task immediately, get any running instances of the task, get or set the credentials that are used to register the task, and the properties that describe the task.</span></span>

## <a name="members"></a><span data-ttu-id="7b804-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7b804-107">Members</span></span>

<span data-ttu-id="7b804-108">El objeto **RegisteredTask** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7b804-108">The **RegisteredTask** object has these types of members:</span></span>

-   [<span data-ttu-id="7b804-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="7b804-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="7b804-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7b804-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7b804-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="7b804-111">Methods</span></span>

<span data-ttu-id="7b804-112">El objeto **RegisteredTask** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7b804-112">The **RegisteredTask** object has these methods.</span></span>



| <span data-ttu-id="7b804-113">Método</span><span class="sxs-lookup"><span data-stu-id="7b804-113">Method</span></span>                                                                | <span data-ttu-id="7b804-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b804-114">Description</span></span>                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b804-115">**GetInstances**</span><span class="sxs-lookup"><span data-stu-id="7b804-115">**GetInstances**</span></span>](registeredtask-getinstances.md)                   | <span data-ttu-id="7b804-116">Devuelve todas las instancias de la tarea registrada que se están ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="7b804-116">Returns all instances of the registered task that are currently running.</span></span><br/>             |
| [<span data-ttu-id="7b804-117">**GetRunTimes**</span><span class="sxs-lookup"><span data-stu-id="7b804-117">**GetRunTimes**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | <span data-ttu-id="7b804-118">Obtiene la hora a la que la tarea registrada está programada para ejecutarse durante un período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="7b804-118">Gets the times that the registered task is scheduled to run during a specified time.</span></span><br/> |
| [<span data-ttu-id="7b804-119">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7b804-119">**GetSecurityDescriptor**</span></span>](registeredtask-getsecuritydescriptor.md) | <span data-ttu-id="7b804-120">Obtiene el descriptor de seguridad que se usa como credenciales para la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="7b804-120">Gets the security descriptor that is used as credentials for the registered task.</span></span><br/>    |
| [<span data-ttu-id="7b804-121">**Ejecutar**</span><span class="sxs-lookup"><span data-stu-id="7b804-121">**Run**</span></span>](registeredtask-run.md)                                     | <span data-ttu-id="7b804-122">Ejecuta la tarea registrada inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="7b804-122">Runs the registered task immediately.</span></span><br/>                                                |
| [<span data-ttu-id="7b804-123">**RunEx**</span><span class="sxs-lookup"><span data-stu-id="7b804-123">**RunEx**</span></span>](registeredtask-runex.md)                                 | <span data-ttu-id="7b804-124">Ejecuta la tarea registrada inmediatamente con las marcas especificadas y un identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="7b804-124">Runs the registered task immediately using specified flags and a session identifier.</span></span><br/> |
| [<span data-ttu-id="7b804-125">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7b804-125">**SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md) | <span data-ttu-id="7b804-126">Establece el descriptor de seguridad que se usa como credenciales para la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="7b804-126">Sets the security descriptor that is used as credentials for the registered task.</span></span><br/>    |
| [<span data-ttu-id="7b804-127">**Stop**</span><span class="sxs-lookup"><span data-stu-id="7b804-127">**Stop**</span></span>](registeredtask-stop.md)                                   | <span data-ttu-id="7b804-128">Detiene inmediatamente la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="7b804-128">Stops the registered task immediately.</span></span><br/>                                               |



 

### <a name="properties"></a><span data-ttu-id="7b804-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7b804-129">Properties</span></span>

<span data-ttu-id="7b804-130">El objeto **RegisteredTask** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7b804-130">The **RegisteredTask** object has these properties.</span></span>



| <span data-ttu-id="7b804-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7b804-131">Property</span></span>                                                                   | <span data-ttu-id="7b804-132">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="7b804-132">Access type</span></span>           | <span data-ttu-id="7b804-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b804-133">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b804-134">**Definición**</span><span class="sxs-lookup"><span data-stu-id="7b804-134">**Definition**</span></span>](registeredtask-definition.md)<br/>                 | <span data-ttu-id="7b804-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b804-135">Read-only</span></span><br/>  | <span data-ttu-id="7b804-136">Obtiene la definición de la tarea.</span><span class="sxs-lookup"><span data-stu-id="7b804-136">Gets the definition of the task.</span></span><br/>                                               |
| [<span data-ttu-id="7b804-137">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="7b804-137">**Enabled**</span></span>](registeredtask-enabled.md)<br/>                       | <span data-ttu-id="7b804-138">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7b804-138">Read/write</span></span><br/> | <span data-ttu-id="7b804-139">Obtiene o establece un valor booleano que indica si la tarea registrada está habilitada.</span><span class="sxs-lookup"><span data-stu-id="7b804-139">Gets or set a Boolean value that indicates if the registered task is enabled.</span></span><br/>  |
| [<span data-ttu-id="7b804-140">**LastRunTime**</span><span class="sxs-lookup"><span data-stu-id="7b804-140">**LastRunTime**</span></span>](registeredtask-lastruntime.md)<br/>               | <span data-ttu-id="7b804-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b804-141">Read-only</span></span><br/>  | <span data-ttu-id="7b804-142">Obtiene la hora en que se ejecutó la tarea registrada por última vez.</span><span class="sxs-lookup"><span data-stu-id="7b804-142">Gets the time the registered task was last run.</span></span><br/>                                |
| [<span data-ttu-id="7b804-143">**LastTaskResult**</span><span class="sxs-lookup"><span data-stu-id="7b804-143">**LastTaskResult**</span></span>](registeredtask-lasttaskresult.md)<br/>         | <span data-ttu-id="7b804-144">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b804-144">Read-only</span></span><br/>  | <span data-ttu-id="7b804-145">Obtiene los resultados que se devolvieron la última vez que se ejecutó la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="7b804-145">Gets the results that were returned the last time the registered task was run.</span></span><br/> |
| [<span data-ttu-id="7b804-146">**Name**</span><span class="sxs-lookup"><span data-stu-id="7b804-146">**Name**</span></span>](registeredtask-name.md)<br/>                             | <span data-ttu-id="7b804-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b804-147">Read-only</span></span><br/>  | <span data-ttu-id="7b804-148">Obtiene el nombre de la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="7b804-148">Gets the name of the registered task.</span></span><br/>                                          |
| [<span data-ttu-id="7b804-149">**NextRunTime**</span><span class="sxs-lookup"><span data-stu-id="7b804-149">**NextRunTime**</span></span>](registeredtask-nextruntime.md)<br/>               | <span data-ttu-id="7b804-150">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b804-150">Read-only</span></span><br/>  | <span data-ttu-id="7b804-151">Obtiene la hora a la que se programa la próxima ejecución de la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="7b804-151">Gets the time when the registered task is next scheduled to run.</span></span><br/>               |
| [<span data-ttu-id="7b804-152">**NumberOfMissedRuns**</span><span class="sxs-lookup"><span data-stu-id="7b804-152">**NumberOfMissedRuns**</span></span>](registeredtask-numberofmissedruns.md)<br/> | <span data-ttu-id="7b804-153">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b804-153">Read-only</span></span><br/>  | <span data-ttu-id="7b804-154">Obtiene el número de veces que la tarea registrada ha perdido una ejecución programada.</span><span class="sxs-lookup"><span data-stu-id="7b804-154">Gets the number of times the registered task has missed a scheduled run.</span></span><br/>       |
| [<span data-ttu-id="7b804-155">**Ruta**</span><span class="sxs-lookup"><span data-stu-id="7b804-155">**Path**</span></span>](registeredtask-path.md)<br/>                             | <span data-ttu-id="7b804-156">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b804-156">Read-only</span></span><br/>  | <span data-ttu-id="7b804-157">Obtiene la ruta de acceso donde se almacena la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="7b804-157">Gets the path to where the registered task is stored.</span></span><br/>                          |
| [<span data-ttu-id="7b804-158">**State**</span><span class="sxs-lookup"><span data-stu-id="7b804-158">**State**</span></span>](registeredtask-state.md)<br/>                           | <span data-ttu-id="7b804-159">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b804-159">Read-only</span></span><br/>  | <span data-ttu-id="7b804-160">Obtiene el estado operativo de la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="7b804-160">Gets the operational state of the registered task.</span></span><br/>                             |
| [<span data-ttu-id="7b804-161">**XML**</span><span class="sxs-lookup"><span data-stu-id="7b804-161">**XML**</span></span>](registeredtask-xml.md)<br/>                               | <span data-ttu-id="7b804-162">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b804-162">Read-only</span></span><br/>  | <span data-ttu-id="7b804-163">Obtiene la información de registro con formato XML para la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="7b804-163">Gets the XML-formatted registration information for the registered task.</span></span><br/>       |



 

## <a name="examples"></a><span data-ttu-id="7b804-164">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7b804-164">Examples</span></span>

<span data-ttu-id="7b804-165">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md) y [Mostrar los nombres y Estados de las tareas (scripting)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="7b804-165">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) and [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b804-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b804-166">Requirements</span></span>



| <span data-ttu-id="7b804-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b804-167">Requirement</span></span> | <span data-ttu-id="7b804-168">Value</span><span class="sxs-lookup"><span data-stu-id="7b804-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b804-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b804-169">Minimum supported client</span></span><br/> | <span data-ttu-id="7b804-170">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7b804-170">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7b804-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b804-171">Minimum supported server</span></span><br/> | <span data-ttu-id="7b804-172">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7b804-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7b804-173">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7b804-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="7b804-174"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7b804-174"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7b804-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7b804-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b804-176"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b804-176"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





