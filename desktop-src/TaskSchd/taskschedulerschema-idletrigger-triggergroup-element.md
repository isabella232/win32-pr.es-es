---
title: Elemento IdleTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando el equipo entra en un estado de inactividad.
ms.assetid: c3e317b5-d1a7-46de-ace5-e066452583d3
keywords:
- desencadenador inactivo, elemento XML
- Programador de tareas del elemento IdleTrigger
topic_type:
- apiref
api_name:
- IdleTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 221d272145670b9514cde5ffbe8b02e5ddcd6e0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079046"
---
# <a name="idletrigger-triggergroup-element"></a><span data-ttu-id="df472-105">Elemento IdleTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="df472-105">IdleTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="df472-106">Especifica un desencadenador que inicia una tarea cuando el equipo entra en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="df472-106">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span> <span data-ttu-id="df472-107">Para obtener información sobre las condiciones de inactividad, consulte [condiciones de inactividad de tareas](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="df472-107">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

``` syntax
<xs:element name="IdleTrigger"
    type="idleTriggerType"
 />
```

<span data-ttu-id="df472-108">El elemento **IdleTrigger** se define mediante [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="df472-108">The **IdleTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="df472-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="df472-109">Parent element</span></span>



| <span data-ttu-id="df472-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="df472-110">Element</span></span>                                                           | <span data-ttu-id="df472-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="df472-111">Derived from</span></span>                                                         | <span data-ttu-id="df472-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="df472-112">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="df472-113">**Desencadenadores**</span><span class="sxs-lookup"><span data-stu-id="df472-113">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="df472-114">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="df472-114">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="df472-115">Especifica los desencadenadores que inician la tarea.</span><span class="sxs-lookup"><span data-stu-id="df472-115">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="df472-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="df472-116">Child elements</span></span>



| <span data-ttu-id="df472-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="df472-117">Element</span></span>                                                                                                        | <span data-ttu-id="df472-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="df472-118">Type</span></span>                                                                     | <span data-ttu-id="df472-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="df472-119">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df472-120">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="df472-120">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="df472-121">boolean</span><span class="sxs-lookup"><span data-stu-id="df472-121">boolean</span></span>                                                                  | <span data-ttu-id="df472-122">Especifica que el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="df472-122">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="df472-123">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="df472-123">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="df472-124">dateTime</span><span class="sxs-lookup"><span data-stu-id="df472-124">dateTime</span></span>                                                                 | <span data-ttu-id="df472-125">Especifica la fecha y hora de desactivación del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="df472-125">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="df472-126">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="df472-126">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="df472-127">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="df472-127">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="df472-128">duration</span><span class="sxs-lookup"><span data-stu-id="df472-128">duration</span></span>                                                                 | <span data-ttu-id="df472-129">Especifica la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="df472-129">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="df472-130">**Repetición (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="df472-130">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="df472-131">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="df472-131">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="df472-132">Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="df472-132">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="df472-133">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="df472-133">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="df472-134">dateTime</span><span class="sxs-lookup"><span data-stu-id="df472-134">dateTime</span></span>                                                                 | <span data-ttu-id="df472-135">Especifica la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="df472-135">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="df472-136">Atributos</span><span class="sxs-lookup"><span data-stu-id="df472-136">Attributes</span></span>



| <span data-ttu-id="df472-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="df472-137">Name</span></span> | <span data-ttu-id="df472-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="df472-138">Type</span></span>   | <span data-ttu-id="df472-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="df472-139">Description</span></span>                               |
|------|--------|-------------------------------------------|
| <span data-ttu-id="df472-140">Identificador</span><span class="sxs-lookup"><span data-stu-id="df472-140">Id</span></span>   | <span data-ttu-id="df472-141">string</span><span class="sxs-lookup"><span data-stu-id="df472-141">string</span></span> | <span data-ttu-id="df472-142">Identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="df472-142">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="df472-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df472-143">Remarks</span></span>

<span data-ttu-id="df472-144">Para el desarrollo de scripting, se especifica un desencadenador inactivo mediante el objeto [**IdleTrigger**](idletrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="df472-144">For scripting development, an idle trigger is specified using the [**IdleTrigger**](idletrigger.md) object.</span></span>

<span data-ttu-id="df472-145">En el desarrollo de C++, se especifica un desencadenador inactivo mediante la interfaz [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) .</span><span class="sxs-lookup"><span data-stu-id="df472-145">For C++ development, an idle trigger is specified using the [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) interface.</span></span>

<span data-ttu-id="df472-146">Los elementos secundarios enumerados anteriormente se definen mediante los tipos de elementos complejos de [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="df472-146">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span> <span data-ttu-id="df472-147">Estos elementos se deben agregar en la secuencia que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="df472-147">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="df472-148">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="df472-148">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="df472-149">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="df472-149">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="df472-150">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="df472-150">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="df472-151">**Repetición (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="df472-151">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="df472-152">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="df472-152">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a><span data-ttu-id="df472-153">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="df472-153">Examples</span></span>

<span data-ttu-id="df472-154">En el código XML siguiente se define un desencadenador idle.</span><span class="sxs-lookup"><span data-stu-id="df472-154">The following XML defines an idle trigger.</span></span>


```XML
<IdleTrigger>
    <StartBoundary>2005-01-01T00:08:00</StartBoundary>
    <EndBounadry>2007-01-01T00:08:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
</IdleTrigger>
```



## <a name="requirements"></a><span data-ttu-id="df472-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df472-155">Requirements</span></span>



| <span data-ttu-id="df472-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="df472-156">Requirement</span></span> | <span data-ttu-id="df472-157">Value</span><span class="sxs-lookup"><span data-stu-id="df472-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="df472-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df472-158">Minimum supported client</span></span><br/> | <span data-ttu-id="df472-159">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="df472-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="df472-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df472-160">Minimum supported server</span></span><br/> | <span data-ttu-id="df472-161">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="df472-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df472-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="df472-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df472-163">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="df472-163">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="df472-164">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="df472-164">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

