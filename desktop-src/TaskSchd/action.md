---
title: Action (objeto)
description: Objeto de scripting que proporciona las propiedades comunes que heredan todos los objetos de acción.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- Objeto de acción Programador de tareas
- Objeto de acción Programador de tareas, descrito
topic_type:
- apiref
api_name:
- Action
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236b26cc4cfcd10f1e6e6094e4b69928343a9ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534624"
---
# <a name="action-object"></a><span data-ttu-id="65b4d-105">Action (objeto)</span><span class="sxs-lookup"><span data-stu-id="65b4d-105">Action object</span></span>

<span data-ttu-id="65b4d-106">Objeto de scripting que proporciona las propiedades comunes que heredan todos los objetos de acción.</span><span class="sxs-lookup"><span data-stu-id="65b4d-106">Scripting object that provides the common properties that are inherited by all action objects.</span></span> <span data-ttu-id="65b4d-107">El método [**ActionCollection. Create**](actioncollection-create.md) crea un objeto de acción.</span><span class="sxs-lookup"><span data-stu-id="65b4d-107">An action object is created by the [**ActionCollection.Create**](actioncollection-create.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="65b4d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="65b4d-108">Members</span></span>

<span data-ttu-id="65b4d-109">El objeto de **acción** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="65b4d-109">The **Action** object has these types of members:</span></span>

-   [<span data-ttu-id="65b4d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="65b4d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65b4d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="65b4d-111">Properties</span></span>

<span data-ttu-id="65b4d-112">El objeto de **acción** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="65b4d-112">The **Action** object has these properties.</span></span>



| <span data-ttu-id="65b4d-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="65b4d-113">Property</span></span>                               | <span data-ttu-id="65b4d-114">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="65b4d-114">Access type</span></span>           | <span data-ttu-id="65b4d-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="65b4d-115">Description</span></span>                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [<span data-ttu-id="65b4d-116">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="65b4d-116">**Id**</span></span>](action-id.md)<br/>     | <span data-ttu-id="65b4d-117">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65b4d-117">Read/write</span></span><br/> | <span data-ttu-id="65b4d-118">Obtiene o establece el identificador de la acción.</span><span class="sxs-lookup"><span data-stu-id="65b4d-118">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="65b4d-119">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="65b4d-119">**Type**</span></span>](action-type.md)<br/> | <span data-ttu-id="65b4d-120">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="65b4d-120">Read-only</span></span><br/>  | <span data-ttu-id="65b4d-121">Obtiene el tipo de la acción.</span><span class="sxs-lookup"><span data-stu-id="65b4d-121">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="65b4d-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65b4d-122">Remarks</span></span>

<span data-ttu-id="65b4d-123">Para obtener información sobre cómo funcionan conjuntamente las acciones y tareas, vea [acciones de tarea](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="65b4d-123">For information on how actions and tasks work together, see [Task Actions](task-actions.md).</span></span> <span data-ttu-id="65b4d-124">La tabla siguiente contiene los objetos de scripting que representan las acciones que se pueden realizar:</span><span class="sxs-lookup"><span data-stu-id="65b4d-124">The following table contains the scripting objects that represent the actions that can be performed:</span></span>



| <span data-ttu-id="65b4d-125">API</span><span class="sxs-lookup"><span data-stu-id="65b4d-125">API</span></span>                                            | <span data-ttu-id="65b4d-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="65b4d-126">Description</span></span>                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="65b4d-127">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="65b4d-127">**ComHandlerAction**</span></span>](comhandleraction.md)   | <span data-ttu-id="65b4d-128">Representa una acción que activa un controlador.</span><span class="sxs-lookup"><span data-stu-id="65b4d-128">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="65b4d-129">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="65b4d-129">**ExecAction**</span></span>](execaction.md)               | <span data-ttu-id="65b4d-130">Representa una acción que ejecuta una operación de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="65b4d-130">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="65b4d-131">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="65b4d-131">**EmailAction**</span></span>](emailaction.md)             | <span data-ttu-id="65b4d-132">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="65b4d-132">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="65b4d-133">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="65b4d-133">**ShowMessageAction**</span></span>](showmessageaction.md) | <span data-ttu-id="65b4d-134">Representa una acción que muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="65b4d-134">Represents an action that shows a message box.</span></span>               |



 

<span data-ttu-id="65b4d-135">Al leer o escribir XML, las acciones de una tarea se especifican en el elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) del esquema programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="65b4d-135">When reading or writing XML, the actions of a task are specified in the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="65b4d-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="65b4d-136">Examples</span></span>

<span data-ttu-id="65b4d-137">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md) , ejemplo de desencadenador de [eventos (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))scripting), ejemplo de [desencadenador diario (](daily-trigger-example--scripting-.md)scripting), ejemplo [de](boot-trigger-example--scripting-.md) [desencadenador de registro (](registration-trigger-example--scripting-.md)scripting), ejemplo de [desencadenador semanal (](weekly-trigger-example--scripting-.md)scripting), ejemplo de [desencadenador de inicio de sesión](logon-trigger-example--scripting-.md)</span><span class="sxs-lookup"><span data-stu-id="65b4d-137">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) , [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65b4d-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65b4d-138">Requirements</span></span>



| <span data-ttu-id="65b4d-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="65b4d-139">Requirement</span></span> | <span data-ttu-id="65b4d-140">Value</span><span class="sxs-lookup"><span data-stu-id="65b4d-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65b4d-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65b4d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="65b4d-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="65b4d-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="65b4d-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65b4d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="65b4d-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="65b4d-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65b4d-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="65b4d-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="65b4d-146"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="65b4d-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="65b4d-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65b4d-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65b4d-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65b4d-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65b4d-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="65b4d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b4d-150">Programador de tareas objetos de scripting</span><span class="sxs-lookup"><span data-stu-id="65b4d-150">Task Scheduler Scripting Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="65b4d-151">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="65b4d-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





