---
title: Objeto TaskFolder
description: Objeto de scripting que proporciona los métodos que se usan para registrar (crear) tareas en la carpeta, quitar tareas de la carpeta y crear o quitar subcarpetas de la carpeta.
ms.assetid: f6fd09ec-2777-4903-83b5-e3ac1aa472a0
keywords:
- Objeto TaskFolder Programador de tareas
- Programador de tareas de objeto TaskFolder, descrito
topic_type:
- apiref
api_name:
- TaskFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ccad9331cf3df12ea5752fdd7e5ac94bfbeba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534984"
---
# <a name="taskfolder-object"></a><span data-ttu-id="4c339-105">Objeto TaskFolder</span><span class="sxs-lookup"><span data-stu-id="4c339-105">TaskFolder object</span></span>

<span data-ttu-id="4c339-106">Objeto de scripting que proporciona los métodos que se usan para registrar (crear) tareas en la carpeta, quitar tareas de la carpeta y crear o quitar subcarpetas de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4c339-106">Scripting object that provides the methods that are used to register (create) tasks in the folder, remove tasks from the folder, and create or remove subfolders from the folder.</span></span>

## <a name="members"></a><span data-ttu-id="4c339-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4c339-107">Members</span></span>

<span data-ttu-id="4c339-108">El objeto **TaskFolder** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4c339-108">The **TaskFolder** object has these types of members:</span></span>

-   [<span data-ttu-id="4c339-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="4c339-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="4c339-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4c339-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4c339-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4c339-111">Methods</span></span>

<span data-ttu-id="4c339-112">El objeto **TaskFolder** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4c339-112">The **TaskFolder** object has these methods.</span></span>



| <span data-ttu-id="4c339-113">Método</span><span class="sxs-lookup"><span data-stu-id="4c339-113">Method</span></span>                                                              | <span data-ttu-id="4c339-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c339-114">Description</span></span>                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c339-115">**CreateFolder**</span><span class="sxs-lookup"><span data-stu-id="4c339-115">**CreateFolder**</span></span>](taskfolder-createfolder.md)                     | <span data-ttu-id="4c339-116">Crea una carpeta para las tareas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4c339-116">Creates a folder for related tasks.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="4c339-117">**DeleteFolder**</span><span class="sxs-lookup"><span data-stu-id="4c339-117">**DeleteFolder**</span></span>](taskfolder-deletefolder.md)                     | <span data-ttu-id="4c339-118">Elimina una subcarpeta de la carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="4c339-118">Deletes a subfolder from the parent folder.</span></span><br/>                                                                                         |
| [<span data-ttu-id="4c339-119">**DeleteTask**</span><span class="sxs-lookup"><span data-stu-id="4c339-119">**DeleteTask**</span></span>](taskfolder-deletetask.md)                         | <span data-ttu-id="4c339-120">Elimina una tarea de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4c339-120">Deletes a task from the folder.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="4c339-121">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="4c339-121">**GetFolder**</span></span>](taskfolder-getfolder.md)                           | <span data-ttu-id="4c339-122">Obtiene una carpeta que contiene tareas en una ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="4c339-122">Gets a folder that contains tasks at a specified location.</span></span><br/>                                                                          |
| [<span data-ttu-id="4c339-123">**GetFolders**</span><span class="sxs-lookup"><span data-stu-id="4c339-123">**GetFolders**</span></span>](taskfolder-getfolders.md)                         | <span data-ttu-id="4c339-124">Obtiene todas las subcarpetas de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4c339-124">Gets all the subfolders in the folder.</span></span><br/>                                                                                              |
| [<span data-ttu-id="4c339-125">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4c339-125">**GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)   | <span data-ttu-id="4c339-126">Obtiene el descriptor de seguridad de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4c339-126">Gets the security descriptor for the folder.</span></span><br/>                                                                                        |
| [<span data-ttu-id="4c339-127">**GetTask**</span><span class="sxs-lookup"><span data-stu-id="4c339-127">**GetTask**</span></span>](taskfolder-gettask.md)                               | <span data-ttu-id="4c339-128">Obtiene una tarea en una ubicación especificada de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4c339-128">Gets a task at a specified location in a folder.</span></span><br/>                                                                                    |
| [<span data-ttu-id="4c339-129">**GetTasks**</span><span class="sxs-lookup"><span data-stu-id="4c339-129">**GetTasks**</span></span>](taskfolder-gettasks.md)                             | <span data-ttu-id="4c339-130">Obtiene todas las tareas de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4c339-130">Gets all the tasks in the folder.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="4c339-131">**RegisterTask**</span><span class="sxs-lookup"><span data-stu-id="4c339-131">**RegisterTask**</span></span>](taskfolder-registertask.md)                     | <span data-ttu-id="4c339-132">Registra (crea) una nueva tarea en la carpeta utilizando XML para definir la tarea.</span><span class="sxs-lookup"><span data-stu-id="4c339-132">Registers (creates) a new task in the folder using XML to define the task.</span></span><br/>                                                          |
| [<span data-ttu-id="4c339-133">**RegisterTaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="4c339-133">**RegisterTaskDefinition**</span></span>](taskfolder-registertaskdefinition.md) | <span data-ttu-id="4c339-134">Registra (crea) una tarea en una ubicación especificada mediante la interfaz [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) para definir una tarea.</span><span class="sxs-lookup"><span data-stu-id="4c339-134">Registers (creates) a task in a specified location using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define a task.</span></span><br/> |
| [<span data-ttu-id="4c339-135">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4c339-135">**SetSecurityDescriptor**</span></span>](taskfolder-setsecuritydescriptor.md)   | <span data-ttu-id="4c339-136">Establece el descriptor de seguridad de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4c339-136">Sets the security descriptor for the folder.</span></span><br/>                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="4c339-137">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4c339-137">Properties</span></span>

<span data-ttu-id="4c339-138">El objeto **TaskFolder** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4c339-138">The **TaskFolder** object has these properties.</span></span>



| <span data-ttu-id="4c339-139">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4c339-139">Property</span></span>                                   | <span data-ttu-id="4c339-140">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="4c339-140">Access type</span></span>          | <span data-ttu-id="4c339-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c339-141">Description</span></span>                                                                        |
|:-------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="4c339-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="4c339-142">**Name**</span></span>](taskfolder-name.md)<br/> | <span data-ttu-id="4c339-143">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c339-143">Read-only</span></span><br/> | <span data-ttu-id="4c339-144">Obtiene el nombre que se usa para identificar la carpeta que contiene una tarea.</span><span class="sxs-lookup"><span data-stu-id="4c339-144">Gets the name that is used to identify the folder that contains a task.</span></span><br/> |
| [<span data-ttu-id="4c339-145">**Ruta**</span><span class="sxs-lookup"><span data-stu-id="4c339-145">**Path**</span></span>](taskfolder-path.md)<br/> | <span data-ttu-id="4c339-146">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c339-146">Read-only</span></span><br/> | <span data-ttu-id="4c339-147">Obtiene la ruta de acceso donde se almacena la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4c339-147">Gets the path to where the folder is stored.</span></span><br/>                            |



 

## <a name="examples"></a><span data-ttu-id="4c339-148">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4c339-148">Examples</span></span>

<span data-ttu-id="4c339-149">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md), [ejemplo de desencadenador de eventos (scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), ejemplo de [desencadenador diario (](daily-trigger-example--scripting-.md)scripting), ejemplo de [desencadenador de registro (scripting](registration-trigger-example--scripting-.md)), [ejemplo de desencadenador semanal (scripting)](weekly-trigger-example--scripting-.md), [ejemplo de desencadenador de inicio de sesión (](logon-trigger-example--scripting-.md)scripting), [ejemplo de desencadenador de arranque (](boot-trigger-example--scripting-.md)scripting) o [visualización](displaying-task-names-and-state--scripting-.md)de</span><span class="sxs-lookup"><span data-stu-id="4c339-149">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md), or [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c339-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c339-150">Requirements</span></span>



| <span data-ttu-id="4c339-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c339-151">Requirement</span></span> | <span data-ttu-id="4c339-152">Value</span><span class="sxs-lookup"><span data-stu-id="4c339-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c339-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c339-153">Minimum supported client</span></span><br/> | <span data-ttu-id="4c339-154">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4c339-154">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4c339-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c339-155">Minimum supported server</span></span><br/> | <span data-ttu-id="4c339-156">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4c339-156">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4c339-157">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4c339-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="4c339-158"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4c339-158"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4c339-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4c339-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c339-160"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c339-160"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c339-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c339-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c339-162">Objetos Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="4c339-162">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="4c339-163">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="4c339-163">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





