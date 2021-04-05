---
title: Elemento LogonTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.
ms.assetid: c3edee50-e053-4813-a1b2-bf1e7b575ff7
keywords:
- desencadenador Logon, elemento XML
- Programador de tareas del elemento LogonTrigger
topic_type:
- apiref
api_name:
- LogonTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89d0e593277f1c854850017412b49c22d8ac436
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359707"
---
# <a name="logontrigger-triggergroup-element"></a><span data-ttu-id="ebd52-105">Elemento LogonTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="ebd52-105">LogonTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="ebd52-106">Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="ebd52-106">Specifies a trigger that starts a task when a user logs on.</span></span>

``` syntax
<xs:element name="LogonTrigger"
    type="logonTriggerType"
 />
```

<span data-ttu-id="ebd52-107">El elemento **LogonTrigger** se define mediante [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="ebd52-107">The **LogonTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="ebd52-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="ebd52-108">Parent element</span></span>



| <span data-ttu-id="ebd52-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="ebd52-109">Element</span></span>                                                           | <span data-ttu-id="ebd52-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="ebd52-110">Derived from</span></span>                                                         | <span data-ttu-id="ebd52-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebd52-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="ebd52-112">**Desencadenadores**</span><span class="sxs-lookup"><span data-stu-id="ebd52-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="ebd52-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="ebd52-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="ebd52-114">Especifica los desencadenadores que inician la tarea.</span><span class="sxs-lookup"><span data-stu-id="ebd52-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="ebd52-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ebd52-115">Child elements</span></span>



| <span data-ttu-id="ebd52-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="ebd52-116">Element</span></span>                                                                                                        | <span data-ttu-id="ebd52-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="ebd52-117">Type</span></span>                                                                     | <span data-ttu-id="ebd52-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebd52-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ebd52-119">**Retraso (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="ebd52-119">**Delay (logonTriggerType)**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)                         | <span data-ttu-id="ebd52-120">duration</span><span class="sxs-lookup"><span data-stu-id="ebd52-120">duration</span></span>                                                                 | <span data-ttu-id="ebd52-121">Cantidad de tiempo entre el momento en el que el usuario inicia sesión y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="ebd52-121">Amount of time between when the user logs on and when the task is started.</span></span><br/>                                              |
| [<span data-ttu-id="ebd52-122">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="ebd52-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="ebd52-123">boolean</span><span class="sxs-lookup"><span data-stu-id="ebd52-123">boolean</span></span>                                                                  | <span data-ttu-id="ebd52-124">Especifica que el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="ebd52-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="ebd52-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="ebd52-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="ebd52-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="ebd52-126">dateTime</span></span>                                                                 | <span data-ttu-id="ebd52-127">Especifica la fecha y hora de desactivación del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="ebd52-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="ebd52-128">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="ebd52-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="ebd52-129">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="ebd52-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="ebd52-130">duration</span><span class="sxs-lookup"><span data-stu-id="ebd52-130">duration</span></span>                                                                 | <span data-ttu-id="ebd52-131">Especifica la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="ebd52-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="ebd52-132">**Repetición (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="ebd52-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="ebd52-133">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="ebd52-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="ebd52-134">Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="ebd52-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="ebd52-135">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="ebd52-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="ebd52-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="ebd52-136">dateTime</span></span>                                                                 | <span data-ttu-id="ebd52-137">Especifica la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="ebd52-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="ebd52-138">**UserId (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="ebd52-138">**UserId (logonTriggerType)**</span></span>](taskschedulerschema-userid-logontriggertype-element.md)                       | <span data-ttu-id="ebd52-139">string</span><span class="sxs-lookup"><span data-stu-id="ebd52-139">string</span></span>                                                                   | <span data-ttu-id="ebd52-140">Identificador del usuario.</span><span class="sxs-lookup"><span data-stu-id="ebd52-140">Identifier of the user.</span></span> <span data-ttu-id="ebd52-141">La tarea se inicia cuando este usuario inicia sesión en el equipo.</span><span class="sxs-lookup"><span data-stu-id="ebd52-141">The task is started when this user logs onto the computer.</span></span><br/>                                      |



## <a name="remarks"></a><span data-ttu-id="ebd52-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ebd52-142">Remarks</span></span>

<span data-ttu-id="ebd52-143">Para el desarrollo de scripting, se especifica un desencadenador Logon mediante el objeto [**LogonTrigger**](logontrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="ebd52-143">For scripting development, a logon trigger is specified using the [**LogonTrigger**](logontrigger.md) object.</span></span>

<span data-ttu-id="ebd52-144">En el desarrollo de C++, se especifica un desencadenador Logon mediante la interfaz [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) .</span><span class="sxs-lookup"><span data-stu-id="ebd52-144">For C++ development, a logon trigger is specified using the [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) interface.</span></span>

<span data-ttu-id="ebd52-145">Los elementos secundarios enumerados anteriormente se definen mediante los tipos de elementos complejos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) y [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ebd52-145">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex element types.</span></span> <span data-ttu-id="ebd52-146">Estos elementos se deben agregar en la secuencia que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="ebd52-146">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="ebd52-147">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="ebd52-147">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="ebd52-148">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="ebd52-148">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="ebd52-149">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="ebd52-149">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="ebd52-150">**Repetición (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="ebd52-150">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="ebd52-151">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="ebd52-151">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [<span data-ttu-id="ebd52-152">**UserId (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="ebd52-152">**UserId (logonTriggerType)**</span></span>](taskschedulerschema-userid-logontriggertype-element.md)
-   [<span data-ttu-id="ebd52-153">**Retraso (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="ebd52-153">**Delay (logonTriggerType)**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)

### <a name="attributes"></a><span data-ttu-id="ebd52-154">Atributos</span><span class="sxs-lookup"><span data-stu-id="ebd52-154">Attributes</span></span>

<span data-ttu-id="ebd52-155">El atributo que se muestra a continuación está definido por los tipos de elementos complejos de [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ebd52-155">The attribute listed below is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span>

-   <span data-ttu-id="ebd52-156">ID: identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="ebd52-156">Id: Identifier of the trigger.</span></span>

## <a name="examples"></a><span data-ttu-id="ebd52-157">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ebd52-157">Examples</span></span>

<span data-ttu-id="ebd52-158">Para obtener un ejemplo completo del XML de una tarea que utiliza un desencadenador Logon, vea [ejemplo de desencadenador de inicio de sesión (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="ebd52-158">For a complete example of the XML for a task that uses a logon trigger, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd52-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebd52-159">Requirements</span></span>



| <span data-ttu-id="ebd52-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebd52-160">Requirement</span></span> | <span data-ttu-id="ebd52-161">Value</span><span class="sxs-lookup"><span data-stu-id="ebd52-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ebd52-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebd52-162">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd52-163">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ebd52-163">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ebd52-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebd52-164">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd52-165">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ebd52-165">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebd52-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebd52-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd52-167">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="ebd52-167">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





