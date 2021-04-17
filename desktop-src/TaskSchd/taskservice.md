---
title: Objeto TaskService
description: En el caso de scripting, proporciona acceso al servicio Programador de tareas para administrar tareas registradas.
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- Objeto TaskService Programador de tareas
- Programador de tareas de objeto TaskService, descrito
topic_type:
- apiref
api_name:
- TaskService
- HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 762cd2445c3c6b720bba0f01ae48b787abc1fb38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492263"
---
# <a name="taskservice-object"></a><span data-ttu-id="bee4e-105">Objeto TaskService</span><span class="sxs-lookup"><span data-stu-id="bee4e-105">TaskService object</span></span>

<span data-ttu-id="bee4e-106">En el caso de scripting, proporciona acceso al servicio Programador de tareas para administrar tareas registradas.</span><span class="sxs-lookup"><span data-stu-id="bee4e-106">For scripting, provides access to the Task Scheduler service for managing registered tasks.</span></span>

<span data-ttu-id="bee4e-107">Se debe llamar al método [**TaskService. Connect**](taskservice-connect.md) antes de llamar a cualquiera de los otros métodos **TaskService** .</span><span class="sxs-lookup"><span data-stu-id="bee4e-107">The [**TaskService.Connect**](taskservice-connect.md) method should be called before calling any of the other **TaskService** methods.</span></span>

## <a name="members"></a><span data-ttu-id="bee4e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="bee4e-108">Members</span></span>

<span data-ttu-id="bee4e-109">El objeto **TaskService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bee4e-109">The **TaskService** object has these types of members:</span></span>

-   [<span data-ttu-id="bee4e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="bee4e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="bee4e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bee4e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bee4e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="bee4e-112">Methods</span></span>

<span data-ttu-id="bee4e-113">El objeto **TaskService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bee4e-113">The **TaskService** object has these methods.</span></span>



| <span data-ttu-id="bee4e-114">Método</span><span class="sxs-lookup"><span data-stu-id="bee4e-114">Method</span></span>                                                 | <span data-ttu-id="bee4e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="bee4e-115">Description</span></span>                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bee4e-116">**Conectar**</span><span class="sxs-lookup"><span data-stu-id="bee4e-116">**Connect**</span></span>](taskservice-connect.md)                 | <span data-ttu-id="bee4e-117">Se conecta a un equipo remoto y asocia todas las llamadas subsiguientes en esta interfaz a una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="bee4e-117">Connects to a remote machine and associates all subsequent calls on this interface with a remote session.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="bee4e-118">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="bee4e-118">**GetFolder**</span></span>](taskservice-getfolder.md)             | <span data-ttu-id="bee4e-119">Obtiene la ruta de acceso a una carpeta de tareas registradas.</span><span class="sxs-lookup"><span data-stu-id="bee4e-119">Gets the path to a folder of registered tasks.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="bee4e-120">**GetRunningTasks**</span><span class="sxs-lookup"><span data-stu-id="bee4e-120">**GetRunningTasks**</span></span>](taskservice-getrunningtasks.md) | <span data-ttu-id="bee4e-121">Obtiene una colección de tareas en ejecución.</span><span class="sxs-lookup"><span data-stu-id="bee4e-121">Gets a collection of running tasks.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="bee4e-122">**NewTask**</span><span class="sxs-lookup"><span data-stu-id="bee4e-122">**NewTask**</span></span>](taskservice-newtask.md)                 | <span data-ttu-id="bee4e-123">Devuelve un objeto de definición de tarea vacía que se rellenará con la configuración y las propiedades y, a continuación, se registrará mediante el método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="bee4e-123">Returns an empty task definition object to be filled in with settings and properties and then registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bee4e-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bee4e-124">Properties</span></span>

<span data-ttu-id="bee4e-125">El objeto **TaskService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bee4e-125">The **TaskService** object has these properties.</span></span>



| <span data-ttu-id="bee4e-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bee4e-126">Property</span></span>                                                          | <span data-ttu-id="bee4e-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="bee4e-127">Description</span></span>                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bee4e-128">**Conectado**</span><span class="sxs-lookup"><span data-stu-id="bee4e-128">**Connected**</span></span>](taskservice-connected.md)<br/>             | <span data-ttu-id="bee4e-129">Obtiene un valor booleano que indica si está conectado al servicio de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="bee4e-129">Gets a Boolean value that indicates if you are connected to the Task Scheduler service.</span></span><br/>                          |
| [<span data-ttu-id="bee4e-130">**ConnectedDomain**</span><span class="sxs-lookup"><span data-stu-id="bee4e-130">**ConnectedDomain**</span></span>](taskservice-connecteddomain.md)<br/> | <span data-ttu-id="bee4e-131">Obtiene el nombre del dominio al que está conectado el equipo [**TargetServer**](taskservice-targetserver.md) .</span><span class="sxs-lookup"><span data-stu-id="bee4e-131">Gets the name of the domain to which the [**TargetServer**](taskservice-targetserver.md) computer is connected.</span></span><br/> |
| [<span data-ttu-id="bee4e-132">**ConnectedUser**</span><span class="sxs-lookup"><span data-stu-id="bee4e-132">**ConnectedUser**</span></span>](taskservice-connecteduser.md)<br/>     | <span data-ttu-id="bee4e-133">Obtiene el nombre del usuario que está conectado al servicio de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="bee4e-133">Gets the name of the user that is connected to the Task Scheduler service.</span></span><br/>                                       |
| <span data-ttu-id="bee4e-134">HighestVersion</span><span class="sxs-lookup"><span data-stu-id="bee4e-134">HighestVersion</span></span><br/>                                         | <span data-ttu-id="bee4e-135">Obtiene la versión más alta de Programador de tareas que admite un equipo.</span><span class="sxs-lookup"><span data-stu-id="bee4e-135">Gets the highest version of Task Scheduler that a computer supports.</span></span><br/>                                             |
| [<span data-ttu-id="bee4e-136">**TargetServer**</span><span class="sxs-lookup"><span data-stu-id="bee4e-136">**TargetServer**</span></span>](taskservice-targetserver.md)<br/>       | <span data-ttu-id="bee4e-137">Obtiene el nombre del equipo que está ejecutando el servicio Programador de tareas al que está conectado el usuario.</span><span class="sxs-lookup"><span data-stu-id="bee4e-137">Gets the name of the computer that is running the Task Scheduler service that the user is connected to.</span></span><br/>          |



 

## <a name="examples"></a><span data-ttu-id="bee4e-138">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bee4e-138">Examples</span></span>

<span data-ttu-id="bee4e-139">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md), [ejemplo de desencadenador de eventos (scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), ejemplo de [desencadenador diario (](daily-trigger-example--scripting-.md)scripting), ejemplo de [desencadenador de registro (scripting](registration-trigger-example--scripting-.md)), [ejemplo de desencadenador semanal (scripting)](weekly-trigger-example--scripting-.md), [ejemplo de desencadenador de inicio de sesión (](logon-trigger-example--scripting-.md)scripting), [ejemplo de desencadenador de arranque (](boot-trigger-example--scripting-.md)scripting) o [visualización](displaying-task-names-and-state--scripting-.md)de</span><span class="sxs-lookup"><span data-stu-id="bee4e-139">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md), or [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bee4e-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bee4e-140">Requirements</span></span>



| <span data-ttu-id="bee4e-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="bee4e-141">Requirement</span></span> | <span data-ttu-id="bee4e-142">Value</span><span class="sxs-lookup"><span data-stu-id="bee4e-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bee4e-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bee4e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bee4e-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bee4e-144">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bee4e-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bee4e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bee4e-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bee4e-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bee4e-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bee4e-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="bee4e-148"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bee4e-148"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bee4e-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bee4e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bee4e-150"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bee4e-150"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bee4e-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="bee4e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bee4e-152">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="bee4e-152">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





