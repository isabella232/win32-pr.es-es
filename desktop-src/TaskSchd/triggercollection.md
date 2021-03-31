---
title: Objeto TriggerCollection (Windows. UI. Xaml. h)
description: Objeto de scripting que se utiliza para agregar, quitar y recuperar los desencadenadores de una tarea.
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- desencadenadores Programador de tareas, objeto de colección de desencadenador
- Objeto TriggerCollection Programador de tareas
- Programador de tareas de objeto TriggerCollection, descrito
topic_type:
- apiref
api_name:
- TriggerCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29f7288d8db0b56fc9cc8b3de7ace8c10c13959a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150090"
---
# <a name="triggercollection-object"></a><span data-ttu-id="0dae8-106">Objeto TriggerCollection</span><span class="sxs-lookup"><span data-stu-id="0dae8-106">TriggerCollection object</span></span>

<span data-ttu-id="0dae8-107">Objeto de scripting que se utiliza para agregar, quitar y recuperar los desencadenadores de una tarea.</span><span class="sxs-lookup"><span data-stu-id="0dae8-107">Scripting object that is used to add to, remove from, and retrieve the triggers of a task.</span></span>

## <a name="members"></a><span data-ttu-id="0dae8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0dae8-108">Members</span></span>

<span data-ttu-id="0dae8-109">El objeto **TriggerCollection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0dae8-109">The **TriggerCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="0dae8-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="0dae8-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0dae8-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0dae8-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0dae8-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="0dae8-112">Methods</span></span>

<span data-ttu-id="0dae8-113">El objeto **TriggerCollection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0dae8-113">The **TriggerCollection** object has these methods.</span></span>



| <span data-ttu-id="0dae8-114">Método</span><span class="sxs-lookup"><span data-stu-id="0dae8-114">Method</span></span>                                     | <span data-ttu-id="0dae8-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="0dae8-115">Description</span></span>                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0dae8-116">**Claridad**</span><span class="sxs-lookup"><span data-stu-id="0dae8-116">**Clear**</span></span>](triggercollection-clear.md)   | <span data-ttu-id="0dae8-117">Borra todos los desencadenadores de la colección.</span><span class="sxs-lookup"><span data-stu-id="0dae8-117">Clears all triggers from the collection.</span></span><br/>                                        |
| [<span data-ttu-id="0dae8-118">**A**</span><span class="sxs-lookup"><span data-stu-id="0dae8-118">**Create**</span></span>](triggercollection-create.md) | <span data-ttu-id="0dae8-119">Crea un nuevo desencadenador para la tarea.</span><span class="sxs-lookup"><span data-stu-id="0dae8-119">Creates a new trigger for the task.</span></span><br/>                                             |
| [<span data-ttu-id="0dae8-120">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="0dae8-120">**Remove**</span></span>](triggercollection-remove.md) | <span data-ttu-id="0dae8-121">Quita el desencadenador especificado de la colección de desencadenadores utilizada por la tarea.</span><span class="sxs-lookup"><span data-stu-id="0dae8-121">Removes the specified trigger from the collection of triggers used by the task.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0dae8-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0dae8-122">Properties</span></span>

<span data-ttu-id="0dae8-123">El objeto **TriggerCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0dae8-123">The **TriggerCollection** object has these properties.</span></span>



| <span data-ttu-id="0dae8-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0dae8-124">Property</span></span>                                            | <span data-ttu-id="0dae8-125">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="0dae8-125">Access type</span></span>          | <span data-ttu-id="0dae8-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="0dae8-126">Description</span></span>                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="0dae8-127">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="0dae8-127">**Count**</span></span>](triggercollection-count.md)<br/> | <span data-ttu-id="0dae8-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0dae8-128">Read-only</span></span><br/> | <span data-ttu-id="0dae8-129">Obtiene el número de desencadenadores de la colección.</span><span class="sxs-lookup"><span data-stu-id="0dae8-129">Gets the number of triggers in the collection.</span></span><br/>  |
| [<span data-ttu-id="0dae8-130">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0dae8-130">**Item**</span></span>](triggercollection-item.md)<br/>   | <span data-ttu-id="0dae8-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0dae8-131">Read-only</span></span><br/> | <span data-ttu-id="0dae8-132">Obtiene el desencadenador especificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="0dae8-132">Gets the specified trigger from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0dae8-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0dae8-133">Remarks</span></span>

<span data-ttu-id="0dae8-134">Al leer o escribir XML para una tarea, los desencadenadores de la tarea se especifican en el elemento [**triggers**](taskschedulerschema-triggers-tasktype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="0dae8-134">When reading or writing XML for a task, the triggers for the task are specified in the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="0dae8-135">Para obtener información acerca de cada tipo de desencadenador, consulte [tipos de desencadenador](trigger-types.md).</span><span class="sxs-lookup"><span data-stu-id="0dae8-135">For information about each trigger type see [Trigger Types](trigger-types.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0dae8-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0dae8-136">Examples</span></span>

<span data-ttu-id="0dae8-137">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="0dae8-137">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0dae8-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dae8-138">Requirements</span></span>



| <span data-ttu-id="0dae8-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dae8-139">Requirement</span></span> | <span data-ttu-id="0dae8-140">Value</span><span class="sxs-lookup"><span data-stu-id="0dae8-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dae8-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dae8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0dae8-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0dae8-142">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0dae8-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dae8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0dae8-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0dae8-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0dae8-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0dae8-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dae8-146"><dt>Windows. UI. Xaml. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dae8-146"><dt>Windows.ui.xaml.h</dt></span></span> </dl> |
| <span data-ttu-id="0dae8-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0dae8-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="0dae8-148"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0dae8-148"><dt>Taskschd.tlb</dt></span></span> </dl>      |
| <span data-ttu-id="0dae8-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0dae8-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0dae8-150"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dae8-150"><dt>Taskschd.dll</dt></span></span> </dl>      |



## <a name="see-also"></a><span data-ttu-id="0dae8-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="0dae8-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dae8-152">**Activado**</span><span class="sxs-lookup"><span data-stu-id="0dae8-152">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





