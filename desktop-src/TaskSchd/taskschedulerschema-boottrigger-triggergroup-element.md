---
title: Elemento BootTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando se inicia el sistema.
ms.assetid: c6833547-0daf-4e8a-b8c5-b422827b1d96
keywords:
- desencadenador de arranque Programador de tareas, elemento XML
- Programador de tareas del elemento BootTrigger
topic_type:
- apiref
api_name:
- BootTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb6ccf590893e19340662fd4c47e4aa68047b29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359788"
---
# <a name="boottrigger-triggergroup-element"></a><span data-ttu-id="dfa13-105">Elemento BootTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="dfa13-105">BootTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="dfa13-106">Especifica un desencadenador que inicia una tarea cuando se inicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="dfa13-106">Specifies a trigger that starts a task when the system is booted.</span></span>

``` syntax
<xs:element name="BootTrigger"
    type="bootTriggerType"
 />
```

<span data-ttu-id="dfa13-107">El elemento **BootTrigger** se define mediante el tipo complejo de [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="dfa13-107">The **BootTrigger** element is defined by the [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="dfa13-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="dfa13-108">Parent element</span></span>



| <span data-ttu-id="dfa13-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="dfa13-109">Element</span></span>                                                           | <span data-ttu-id="dfa13-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="dfa13-110">Derived from</span></span>                                                         | <span data-ttu-id="dfa13-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfa13-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="dfa13-112">**Desencadenadores**</span><span class="sxs-lookup"><span data-stu-id="dfa13-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="dfa13-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="dfa13-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="dfa13-114">Especifica los desencadenadores que inician la tarea.</span><span class="sxs-lookup"><span data-stu-id="dfa13-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="dfa13-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dfa13-115">Child elements</span></span>



| <span data-ttu-id="dfa13-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="dfa13-116">Element</span></span>                                                                                                        | <span data-ttu-id="dfa13-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="dfa13-117">Type</span></span>                                                                     | <span data-ttu-id="dfa13-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfa13-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfa13-119">**Retraso (bootTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="dfa13-119">**Delay (bootTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)                           | <span data-ttu-id="dfa13-120">duration</span><span class="sxs-lookup"><span data-stu-id="dfa13-120">duration</span></span>                                                                 | <span data-ttu-id="dfa13-121">Especifica la cantidad de tiempo entre el momento en que se arranca el sistema y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="dfa13-121">Specifies the amount of time between when the system is booted and when the task is started.</span></span><br/>                            |
| [<span data-ttu-id="dfa13-122">**Habilitado (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="dfa13-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="dfa13-123">boolean</span><span class="sxs-lookup"><span data-stu-id="dfa13-123">boolean</span></span>                                                                  | <span data-ttu-id="dfa13-124">Especifica que el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="dfa13-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="dfa13-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="dfa13-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="dfa13-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="dfa13-126">dateTime</span></span>                                                                 | <span data-ttu-id="dfa13-127">Especifica la fecha y hora de desactivación del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="dfa13-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="dfa13-128">El desencadenador no puede iniciar la tarea después de que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="dfa13-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="dfa13-129">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="dfa13-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="dfa13-130">duration</span><span class="sxs-lookup"><span data-stu-id="dfa13-130">duration</span></span>                                                                 | <span data-ttu-id="dfa13-131">Especifica la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="dfa13-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="dfa13-132">**Repetición (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="dfa13-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="dfa13-133">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="dfa13-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="dfa13-134">Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="dfa13-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="dfa13-135">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="dfa13-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="dfa13-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="dfa13-136">dateTime</span></span>                                                                 | <span data-ttu-id="dfa13-137">Especifica la fecha y hora en que se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="dfa13-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="dfa13-138">Atributos</span><span class="sxs-lookup"><span data-stu-id="dfa13-138">Attributes</span></span>



| <span data-ttu-id="dfa13-139">Nombre</span><span class="sxs-lookup"><span data-stu-id="dfa13-139">Name</span></span> | <span data-ttu-id="dfa13-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="dfa13-140">Type</span></span>       | <span data-ttu-id="dfa13-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfa13-141">Description</span></span>                               |
|------|------------|-------------------------------------------|
| <span data-ttu-id="dfa13-142">Identificador</span><span class="sxs-lookup"><span data-stu-id="dfa13-142">Id</span></span>   | <span data-ttu-id="dfa13-143">**string**</span><span class="sxs-lookup"><span data-stu-id="dfa13-143">**string**</span></span> | <span data-ttu-id="dfa13-144">Identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="dfa13-144">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dfa13-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfa13-145">Remarks</span></span>

<span data-ttu-id="dfa13-146">Para el desarrollo de scripts, un desencadenador de arranque se define mediante el objeto [**BootTrigger**](boottrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="dfa13-146">For script development, a boot trigger is defined by the [**BootTrigger**](boottrigger.md) object.</span></span>

<span data-ttu-id="dfa13-147">En el desarrollo de C++, el objeto [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) define un desencadenador de arranque.</span><span class="sxs-lookup"><span data-stu-id="dfa13-147">For C++ development, a boot trigger is defined by the [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) object.</span></span>

## <a name="examples"></a><span data-ttu-id="dfa13-148">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dfa13-148">Examples</span></span>

<span data-ttu-id="dfa13-149">Para obtener un ejemplo completo del XML de una tarea que especifica un desencadenador de arranque, vea [ejemplo de desencadenador de arranque (XML)](boot-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="dfa13-149">For a complete example of the XML for a task that specifies a boot trigger, see [Boot Trigger Example (XML)](boot-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfa13-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfa13-150">Requirements</span></span>



| <span data-ttu-id="dfa13-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfa13-151">Requirement</span></span> | <span data-ttu-id="dfa13-152">Value</span><span class="sxs-lookup"><span data-stu-id="dfa13-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dfa13-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfa13-153">Minimum supported client</span></span><br/> | <span data-ttu-id="dfa13-154">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dfa13-154">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dfa13-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfa13-155">Minimum supported server</span></span><br/> | <span data-ttu-id="dfa13-156">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dfa13-156">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dfa13-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfa13-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa13-158">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="dfa13-158">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="dfa13-159">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="dfa13-159">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





