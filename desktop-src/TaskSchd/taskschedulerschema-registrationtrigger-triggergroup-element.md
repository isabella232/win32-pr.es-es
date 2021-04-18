---
title: Elemento RegistrationTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando se registra la tarea.
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- Programador de tareas de desencadenador de registro, elemento XML
- Programador de tareas del elemento RegistrationTrigger
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90960f81d252b0b0a8d1de3ab5cc1465003467a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686077"
---
# <a name="registrationtrigger-triggergroup-element"></a><span data-ttu-id="e95c8-105">Elemento RegistrationTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="e95c8-105">RegistrationTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="e95c8-106">Especifica un desencadenador que inicia una tarea cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="e95c8-106">Specifies a trigger that starts a task when the task is registered.</span></span>

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

<span data-ttu-id="e95c8-107">El elemento **RegistrationTrigger** se define mediante el tipo complejo de [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e95c8-107">The **RegistrationTrigger** element is defined by the [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e95c8-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="e95c8-108">Parent element</span></span>



| <span data-ttu-id="e95c8-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="e95c8-109">Element</span></span>                                                           | <span data-ttu-id="e95c8-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e95c8-110">Derived from</span></span>                                                         | <span data-ttu-id="e95c8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e95c8-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="e95c8-112">**Desencadenadores**</span><span class="sxs-lookup"><span data-stu-id="e95c8-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="e95c8-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="e95c8-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="e95c8-114">Especifica los desencadenadores que inician la tarea.</span><span class="sxs-lookup"><span data-stu-id="e95c8-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="e95c8-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e95c8-115">Child elements</span></span>



| <span data-ttu-id="e95c8-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="e95c8-116">Element</span></span>                                                                                                        | <span data-ttu-id="e95c8-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="e95c8-117">Type</span></span>                                                                     | <span data-ttu-id="e95c8-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="e95c8-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e95c8-119">**Retraso (registrationTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="e95c8-119">**Delay (registrationTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)                   | <span data-ttu-id="e95c8-120">duration</span><span class="sxs-lookup"><span data-stu-id="e95c8-120">duration</span></span>                                                                 | <span data-ttu-id="e95c8-121">Especifica la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="e95c8-121">Specifies the amount of time between when the task is registered and when the task is started.</span></span><br/>                          |
| [<span data-ttu-id="e95c8-122">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="e95c8-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="e95c8-123">boolean</span><span class="sxs-lookup"><span data-stu-id="e95c8-123">boolean</span></span>                                                                  | <span data-ttu-id="e95c8-124">Especifica que el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e95c8-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="e95c8-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="e95c8-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="e95c8-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="e95c8-126">dateTime</span></span>                                                                 | <span data-ttu-id="e95c8-127">Especifica la fecha y hora de desactivación del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="e95c8-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="e95c8-128">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="e95c8-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="e95c8-129">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="e95c8-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="e95c8-130">duration</span><span class="sxs-lookup"><span data-stu-id="e95c8-130">duration</span></span>                                                                 | <span data-ttu-id="e95c8-131">Especifica la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="e95c8-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="e95c8-132">**Repetición (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="e95c8-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="e95c8-133">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="e95c8-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="e95c8-134">Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="e95c8-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="e95c8-135">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="e95c8-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="e95c8-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="e95c8-136">dateTime</span></span>                                                                 | <span data-ttu-id="e95c8-137">Especifica la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="e95c8-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="e95c8-138">Atributos</span><span class="sxs-lookup"><span data-stu-id="e95c8-138">Attributes</span></span>



| <span data-ttu-id="e95c8-139">Nombre</span><span class="sxs-lookup"><span data-stu-id="e95c8-139">Name</span></span> | <span data-ttu-id="e95c8-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="e95c8-140">Type</span></span> | <span data-ttu-id="e95c8-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="e95c8-141">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="e95c8-142">Identificador</span><span class="sxs-lookup"><span data-stu-id="e95c8-142">Id</span></span>   | <span data-ttu-id="e95c8-143">id</span><span class="sxs-lookup"><span data-stu-id="e95c8-143">ID</span></span>   | <span data-ttu-id="e95c8-144">Identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="e95c8-144">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e95c8-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e95c8-145">Remarks</span></span>

<span data-ttu-id="e95c8-146">Para el desarrollo de scripting, se especifica un desencadenador de registro mediante el objeto [**RegistrationTrigger**](registrationtrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="e95c8-146">For scripting development, a registration trigger is specified using the [**RegistrationTrigger**](registrationtrigger.md) object.</span></span>

<span data-ttu-id="e95c8-147">En el desarrollo de C++, se especifica un desencadenador de registro mediante la interfaz [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) .</span><span class="sxs-lookup"><span data-stu-id="e95c8-147">For C++ development, a registration trigger is specified using the [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) interface.</span></span>

<span data-ttu-id="e95c8-148">Los elementos secundarios enumerados anteriormente se definen mediante los tipos de elementos complejos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) y [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e95c8-148">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex element types.</span></span> <span data-ttu-id="e95c8-149">Estos elementos se deben agregar en la secuencia que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="e95c8-149">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="e95c8-150">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="e95c8-150">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="e95c8-151">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="e95c8-151">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="e95c8-152">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="e95c8-152">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="e95c8-153">**Repetición (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="e95c8-153">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="e95c8-154">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="e95c8-154">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [<span data-ttu-id="e95c8-155">**Retraso (registrationTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="e95c8-155">**Delay (registrationTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a><span data-ttu-id="e95c8-156">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e95c8-156">Examples</span></span>

<span data-ttu-id="e95c8-157">Para obtener un ejemplo completo del XML de una tarea que especifica un desencadenador de arranque, vea [ejemplo de desencadenador de registro (XML)](registration-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="e95c8-157">For a complete example of the XML for a task that specifies a boot trigger, see [Registration Trigger Example (XML)](registration-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e95c8-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e95c8-158">Requirements</span></span>



| <span data-ttu-id="e95c8-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="e95c8-159">Requirement</span></span> | <span data-ttu-id="e95c8-160">Value</span><span class="sxs-lookup"><span data-stu-id="e95c8-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e95c8-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e95c8-161">Minimum supported client</span></span><br/> | <span data-ttu-id="e95c8-162">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e95c8-162">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e95c8-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e95c8-163">Minimum supported server</span></span><br/> | <span data-ttu-id="e95c8-164">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e95c8-164">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e95c8-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="e95c8-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e95c8-166">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="e95c8-166">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e95c8-167">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="e95c8-167">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





