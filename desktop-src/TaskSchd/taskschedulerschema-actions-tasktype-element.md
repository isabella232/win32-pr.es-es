---
title: Elemento Actions (taskType)
description: Contiene las acciones realizadas por la tarea.
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- Programador de tareas del elemento Actions (taskType)
- acciones Programador de tareas, XML
- Elemento Actions Programador de tareas
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21af0f8a06faa9cdc61917dcb3b3b0672c47e0e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422096"
---
# <a name="actions-tasktype-element"></a><span data-ttu-id="0d024-106">Elemento Actions (taskType)</span><span class="sxs-lookup"><span data-stu-id="0d024-106">Actions (taskType) Element</span></span>

<span data-ttu-id="0d024-107">Contiene las acciones realizadas por la tarea.</span><span class="sxs-lookup"><span data-stu-id="0d024-107">Contains the actions performed by the task.</span></span>

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

<span data-ttu-id="0d024-108">El elemento **Actions** se define mediante el tipo complejo [**taskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0d024-108">The **Actions** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0d024-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="0d024-109">Parent element</span></span>



| <span data-ttu-id="0d024-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="0d024-110">Element</span></span>                                          | <span data-ttu-id="0d024-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="0d024-111">Derived from</span></span>                                                 | <span data-ttu-id="0d024-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d024-112">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="0d024-113">**Task**</span><span class="sxs-lookup"><span data-stu-id="0d024-113">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="0d024-114">**taskType**</span><span class="sxs-lookup"><span data-stu-id="0d024-114">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="0d024-115">Describe la tarea que realiza el servicio Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="0d024-115">Describes the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="0d024-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0d024-116">Child elements</span></span>



| <span data-ttu-id="0d024-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="0d024-117">Element</span></span>                                                                    | <span data-ttu-id="0d024-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d024-118">Type</span></span>                                                                       | <span data-ttu-id="0d024-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d024-119">Description</span></span>                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="0d024-120">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="0d024-120">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | [<span data-ttu-id="0d024-121">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="0d024-121">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)   | <span data-ttu-id="0d024-122">Especifica una acción que activa un controlador.</span><span class="sxs-lookup"><span data-stu-id="0d024-122">Specifies an action that fires a handler.</span></span><br/>                   |
| [<span data-ttu-id="0d024-123">**Ejec**</span><span class="sxs-lookup"><span data-stu-id="0d024-123">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | [<span data-ttu-id="0d024-124">**execType**</span><span class="sxs-lookup"><span data-stu-id="0d024-124">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)               | <span data-ttu-id="0d024-125">Especifica una acción que ejecuta una operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="0d024-125">Specifies an action that executes a command-line operation.</span></span><br/> |
| [<span data-ttu-id="0d024-126">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="0d024-126">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | [<span data-ttu-id="0d024-127">**sendEmailType**</span><span class="sxs-lookup"><span data-stu-id="0d024-127">**sendEmailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)     | <span data-ttu-id="0d024-128">Especifica una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0d024-128">Specifies an action that sends an email message.</span></span><br/>            |
| [<span data-ttu-id="0d024-129">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="0d024-129">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="0d024-130">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="0d024-130">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="0d024-131">Especifica una acción que muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="0d024-131">Specifies an action that shows a message box.</span></span><br/>               |



## <a name="attributes"></a><span data-ttu-id="0d024-132">Atributos</span><span class="sxs-lookup"><span data-stu-id="0d024-132">Attributes</span></span>



| <span data-ttu-id="0d024-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="0d024-133">Name</span></span>    | <span data-ttu-id="0d024-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d024-134">Type</span></span> | <span data-ttu-id="0d024-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d024-135">Description</span></span>                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d024-136">Context</span><span class="sxs-lookup"><span data-stu-id="0d024-136">Context</span></span> |      | <span data-ttu-id="0d024-137">Identificador principal del usuario que es el contexto de seguridad para las acciones de la tarea.</span><span class="sxs-lookup"><span data-stu-id="0d024-137">Principal identifier of the user who is the security context for the actions of the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0d024-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d024-138">Remarks</span></span>

<span data-ttu-id="0d024-139">Los elementos secundarios enumerados anteriormente (el máximo 32) se definen mediante el grupo [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="0d024-139">The child elements listed previously (maximum 32) are defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) group.</span></span> <span data-ttu-id="0d024-140">Estos elementos se pueden agregar en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="0d024-140">These elements can be added in any order.</span></span>

<span data-ttu-id="0d024-141">En el desarrollo de C++, las acciones de una tarea se definen en la interfaz [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) .</span><span class="sxs-lookup"><span data-stu-id="0d024-141">For C++ development, the actions of a task are defined in the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface.</span></span>

<span data-ttu-id="0d024-142">Para el desarrollo de scripts, las acciones de una tarea se definen en el objeto [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="0d024-142">For script development, the actions of a task are defined in the [**ActionCollection**](actioncollection.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="0d024-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0d024-143">Examples</span></span>

<span data-ttu-id="0d024-144">Para obtener más información y un ejemplo completo del XML para una tarea que contiene una única acción de ejecución, vea [ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="0d024-144">For more information and a complete example of the XML for a task that contains a single execution action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d024-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d024-145">Requirements</span></span>



| <span data-ttu-id="0d024-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d024-146">Requirement</span></span> | <span data-ttu-id="0d024-147">Value</span><span class="sxs-lookup"><span data-stu-id="0d024-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0d024-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d024-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0d024-149">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0d024-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0d024-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d024-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0d024-151">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d024-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d024-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d024-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d024-153">**taskType**</span><span class="sxs-lookup"><span data-stu-id="0d024-153">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[<span data-ttu-id="0d024-154">**actionGroup**</span><span class="sxs-lookup"><span data-stu-id="0d024-154">**actionGroup**</span></span>](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[<span data-ttu-id="0d024-155">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="0d024-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="0d024-156">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="0d024-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





