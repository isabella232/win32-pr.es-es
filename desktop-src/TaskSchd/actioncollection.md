---
title: Objeto ActionCollection
description: Objeto de scripting que contiene las acciones realizadas por la tarea.
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- Actions Programador de tareas, Collection (objeto)
- Objeto ActionCollection Programador de tareas
- Programador de tareas de objeto ActionCollection, descrito
topic_type:
- apiref
api_name:
- ActionCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dee7182cc79684dec1fd052f7ad67409ba513f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535506"
---
# <a name="actioncollection-object"></a><span data-ttu-id="9dd08-106">Objeto ActionCollection</span><span class="sxs-lookup"><span data-stu-id="9dd08-106">ActionCollection object</span></span>

<span data-ttu-id="9dd08-107">Objeto de scripting que contiene las acciones realizadas por la tarea.</span><span class="sxs-lookup"><span data-stu-id="9dd08-107">Scripting object that contains the actions performed by the task.</span></span>

## <a name="members"></a><span data-ttu-id="9dd08-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9dd08-108">Members</span></span>

<span data-ttu-id="9dd08-109">El objeto **ActionCollection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9dd08-109">The **ActionCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="9dd08-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9dd08-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9dd08-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9dd08-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9dd08-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9dd08-112">Methods</span></span>

<span data-ttu-id="9dd08-113">El objeto **ActionCollection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9dd08-113">The **ActionCollection** object has these methods.</span></span>



| <span data-ttu-id="9dd08-114">Método</span><span class="sxs-lookup"><span data-stu-id="9dd08-114">Method</span></span>                                    | <span data-ttu-id="9dd08-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9dd08-115">Description</span></span>                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="9dd08-116">**Claridad**</span><span class="sxs-lookup"><span data-stu-id="9dd08-116">**Clear**</span></span>](actioncollection-clear.md)   | <span data-ttu-id="9dd08-117">Borra todas las acciones de la colección.</span><span class="sxs-lookup"><span data-stu-id="9dd08-117">Clears all the actions from the collection.</span></span><br/>      |
| [<span data-ttu-id="9dd08-118">**A**</span><span class="sxs-lookup"><span data-stu-id="9dd08-118">**Create**</span></span>](actioncollection-create.md) | <span data-ttu-id="9dd08-119">Crea y agrega una nueva acción a la colección.</span><span class="sxs-lookup"><span data-stu-id="9dd08-119">Creates and adds a new action to the collection.</span></span><br/> |
| [<span data-ttu-id="9dd08-120">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="9dd08-120">**Remove**</span></span>](actioncollection-remove.md) | <span data-ttu-id="9dd08-121">Quita una acción especificada de la colección.</span><span class="sxs-lookup"><span data-stu-id="9dd08-121">Removes a specified action from the collection.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="9dd08-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9dd08-122">Properties</span></span>

<span data-ttu-id="9dd08-123">El objeto **ActionCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9dd08-123">The **ActionCollection** object has these properties.</span></span>



| <span data-ttu-id="9dd08-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9dd08-124">Property</span></span>                                               | <span data-ttu-id="9dd08-125">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="9dd08-125">Access type</span></span>           | <span data-ttu-id="9dd08-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="9dd08-126">Description</span></span>                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="9dd08-127">**Context**</span><span class="sxs-lookup"><span data-stu-id="9dd08-127">**Context**</span></span>](actioncollection-context.md)<br/> | <span data-ttu-id="9dd08-128">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9dd08-128">Read/write</span></span><br/> | <span data-ttu-id="9dd08-129">Obtiene o establece el identificador de la entidad de seguridad para la tarea.</span><span class="sxs-lookup"><span data-stu-id="9dd08-129">Gets or sets the identifier of the principal for the task.</span></span><br/> |
| [<span data-ttu-id="9dd08-130">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="9dd08-130">**Count**</span></span>](actioncollection-count.md)<br/>     | <span data-ttu-id="9dd08-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="9dd08-131">Read-only</span></span><br/>  | <span data-ttu-id="9dd08-132">Obtiene el número de acciones de la colección.</span><span class="sxs-lookup"><span data-stu-id="9dd08-132">Gets the number of actions in the collection.</span></span><br/>              |
| [<span data-ttu-id="9dd08-133">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9dd08-133">**Item**</span></span>](actioncollection-item.md)<br/>       | <span data-ttu-id="9dd08-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="9dd08-134">Read-only</span></span><br/>  | <span data-ttu-id="9dd08-135">Obtiene una acción especificada de la colección.</span><span class="sxs-lookup"><span data-stu-id="9dd08-135">Gets a specified action from the collection.</span></span><br/>               |
| [<span data-ttu-id="9dd08-136">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="9dd08-136">**XmlText**</span></span>](actioncollection-xmltext.md)<br/> | <span data-ttu-id="9dd08-137">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9dd08-137">Read/write</span></span><br/> | <span data-ttu-id="9dd08-138">Obtiene o establece una versión con formato XML de la colección.</span><span class="sxs-lookup"><span data-stu-id="9dd08-138">Gets or sets an XML-formatted version of the collection.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="9dd08-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9dd08-139">Remarks</span></span>

<span data-ttu-id="9dd08-140">Al leer o escribir XML, las acciones de una tarea se especifican en el elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) del esquema programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="9dd08-140">When reading or writing XML, the actions of a task are specified in the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="9dd08-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9dd08-141">Examples</span></span>

<span data-ttu-id="9dd08-142">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md), ejemplo de desencadenador de [eventos (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))scripting), ejemplo de [desencadenador diario (](daily-trigger-example--scripting-.md)scripting), ejemplo [de](boot-trigger-example--scripting-.md) [desencadenador de registro (](registration-trigger-example--scripting-.md)scripting), ejemplo de [desencadenador semanal (](weekly-trigger-example--scripting-.md)scripting), ejemplo de [desencadenador de inicio de sesión](logon-trigger-example--scripting-.md)</span><span class="sxs-lookup"><span data-stu-id="9dd08-142">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd08-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dd08-143">Requirements</span></span>



| <span data-ttu-id="9dd08-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dd08-144">Requirement</span></span> | <span data-ttu-id="9dd08-145">Value</span><span class="sxs-lookup"><span data-stu-id="9dd08-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd08-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dd08-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9dd08-147">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9dd08-147">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9dd08-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dd08-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9dd08-149">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9dd08-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9dd08-150">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9dd08-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="9dd08-151"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9dd08-151"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9dd08-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9dd08-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dd08-153"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dd08-153"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





