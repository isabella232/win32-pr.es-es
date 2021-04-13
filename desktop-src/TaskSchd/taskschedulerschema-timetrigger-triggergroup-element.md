---
title: Elemento TimeTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando se activa el desencadenador.
ms.assetid: bb467f36-47cd-4db4-97c4-60c09937caac
keywords:
- Programador de tareas del elemento TimeTrigger
topic_type:
- apiref
api_name:
- TimeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83d3b0a63a8be70af7eba4edb90e49db71892f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492053"
---
# <a name="timetrigger-triggergroup-element"></a><span data-ttu-id="4970e-104">Elemento TimeTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="4970e-104">TimeTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="4970e-105">Especifica un desencadenador que inicia una tarea cuando se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="4970e-105">Specifies a trigger that starts a task when the trigger is activated.</span></span>

``` syntax
<xs:element name="TimeTrigger"
    type="timeTriggerType"
 />
```

<span data-ttu-id="4970e-106">El elemento **TimeTrigger** se define mediante [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="4970e-106">The **TimeTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="4970e-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="4970e-107">Parent element</span></span>



| <span data-ttu-id="4970e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4970e-108">Element</span></span>                                                           | <span data-ttu-id="4970e-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="4970e-109">Derived from</span></span>                                                         | <span data-ttu-id="4970e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4970e-110">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="4970e-111">**Desencadenadores**</span><span class="sxs-lookup"><span data-stu-id="4970e-111">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="4970e-112">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="4970e-112">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="4970e-113">Especifica los desencadenadores que inician la tarea.</span><span class="sxs-lookup"><span data-stu-id="4970e-113">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="4970e-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4970e-114">Child elements</span></span>



| <span data-ttu-id="4970e-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="4970e-115">Element</span></span>                                                                                                        | <span data-ttu-id="4970e-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="4970e-116">Type</span></span>                                                                     | <span data-ttu-id="4970e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4970e-117">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4970e-118">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="4970e-118">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="4970e-119">boolean</span><span class="sxs-lookup"><span data-stu-id="4970e-119">boolean</span></span>                                                                  | <span data-ttu-id="4970e-120">Especifica que el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="4970e-120">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="4970e-121">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="4970e-121">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="4970e-122">dateTime</span><span class="sxs-lookup"><span data-stu-id="4970e-122">dateTime</span></span>                                                                 | <span data-ttu-id="4970e-123">Especifica la fecha y hora de desactivación del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="4970e-123">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="4970e-124">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="4970e-124">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="4970e-125">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="4970e-125">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="4970e-126">duration</span><span class="sxs-lookup"><span data-stu-id="4970e-126">duration</span></span>                                                                 | <span data-ttu-id="4970e-127">Especifica la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="4970e-127">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="4970e-128">**Repetición (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="4970e-128">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="4970e-129">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="4970e-129">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="4970e-130">Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="4970e-130">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="4970e-131">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="4970e-131">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="4970e-132">dateTime</span><span class="sxs-lookup"><span data-stu-id="4970e-132">dateTime</span></span>                                                                 | <span data-ttu-id="4970e-133">Especifica la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="4970e-133">Specifies the date and time when the trigger is activated.</span></span> <span data-ttu-id="4970e-134">Este elemento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4970e-134">This element is required.</span></span><br/>                                    |



## <a name="attributes"></a><span data-ttu-id="4970e-135">Atributos</span><span class="sxs-lookup"><span data-stu-id="4970e-135">Attributes</span></span>



| <span data-ttu-id="4970e-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="4970e-136">Name</span></span> | <span data-ttu-id="4970e-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="4970e-137">Type</span></span>       | <span data-ttu-id="4970e-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="4970e-138">Description</span></span>                               |
|------|------------|-------------------------------------------|
| <span data-ttu-id="4970e-139">Identificador</span><span class="sxs-lookup"><span data-stu-id="4970e-139">Id</span></span>   | <span data-ttu-id="4970e-140">**string**</span><span class="sxs-lookup"><span data-stu-id="4970e-140">**string**</span></span> | <span data-ttu-id="4970e-141">Identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="4970e-141">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4970e-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4970e-142">Remarks</span></span>

<span data-ttu-id="4970e-143">El elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores de tiempo y calendario (**TimeTrigger** y [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span><span class="sxs-lookup"><span data-stu-id="4970e-143">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers (**TimeTrigger** and [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="4970e-144">Para el desarrollo de scripting, se especifica un desencadenador de tiempo mediante el objeto [**TimeTrigger**](timetrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="4970e-144">For scripting development, a time trigger is specified using the [**TimeTrigger**](timetrigger.md) object.</span></span>

<span data-ttu-id="4970e-145">En el desarrollo de C++, se especifica un desencadenador de tiempo mediante la interfaz [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) .</span><span class="sxs-lookup"><span data-stu-id="4970e-145">For C++ development, a time trigger is specified using the [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) interface.</span></span>

<span data-ttu-id="4970e-146">Los elementos secundarios enumerados anteriormente se definen mediante los tipos de elementos complejos de [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4970e-146">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span> <span data-ttu-id="4970e-147">Estos elementos se deben agregar en la secuencia que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="4970e-147">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="4970e-148">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="4970e-148">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="4970e-149">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="4970e-149">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="4970e-150">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="4970e-150">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="4970e-151">**Repetición (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="4970e-151">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="4970e-152">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="4970e-152">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a><span data-ttu-id="4970e-153">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4970e-153">Examples</span></span>

<span data-ttu-id="4970e-154">Para obtener un ejemplo completo del XML de una tarea que especifica un desencadenador Time, vea [ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="4970e-154">For a complete example of the XML for a task that specifies a time trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4970e-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4970e-155">Requirements</span></span>



| <span data-ttu-id="4970e-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="4970e-156">Requirement</span></span> | <span data-ttu-id="4970e-157">Value</span><span class="sxs-lookup"><span data-stu-id="4970e-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4970e-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4970e-158">Minimum supported client</span></span><br/> | <span data-ttu-id="4970e-159">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4970e-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4970e-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4970e-160">Minimum supported server</span></span><br/> | <span data-ttu-id="4970e-161">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4970e-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4970e-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="4970e-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4970e-163">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="4970e-163">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





