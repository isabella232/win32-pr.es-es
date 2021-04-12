---
title: Elemento repite (triggerBaseType)
description: Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- Elemento repite Programador de tareas
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ebd6f9f77998e5e975e24ff752a475e3880c0aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491669"
---
# <a name="repetition-triggerbasetype-element"></a><span data-ttu-id="d5af7-104">Elemento repite (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="d5af7-104">Repetition (triggerBaseType) Element</span></span>

<span data-ttu-id="d5af7-105">Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.</span><span class="sxs-lookup"><span data-stu-id="d5af7-105">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

<span data-ttu-id="d5af7-106">El tipo complejo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) define el elemento **repite** .</span><span class="sxs-lookup"><span data-stu-id="d5af7-106">The **Repetition** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d5af7-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="d5af7-107">Parent element</span></span>



| <span data-ttu-id="d5af7-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d5af7-108">Element</span></span>                                                                                     | <span data-ttu-id="d5af7-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="d5af7-109">Derived from</span></span>                                                                               | <span data-ttu-id="d5af7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5af7-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5af7-111">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="d5af7-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="d5af7-112">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d5af7-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="d5af7-113">Especifica un desencadenador que inicia una tarea cuando se inicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="d5af7-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="d5af7-114">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="d5af7-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="d5af7-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d5af7-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="d5af7-116">Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.</span><span class="sxs-lookup"><span data-stu-id="d5af7-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="d5af7-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="d5af7-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="d5af7-118">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d5af7-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="d5af7-119">Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="d5af7-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="d5af7-120">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="d5af7-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="d5af7-121">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d5af7-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="d5af7-122">Especifica un desencadenador que inicia una tarea cuando el equipo entra en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="d5af7-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="d5af7-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="d5af7-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="d5af7-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d5af7-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="d5af7-125">Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="d5af7-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="d5af7-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="d5af7-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="d5af7-127">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d5af7-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="d5af7-128">Especifica un desencadenador que inicia una tarea cuando se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="d5af7-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="d5af7-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="d5af7-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="d5af7-130">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d5af7-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="d5af7-131">Especifica un desencadenador que inicia una tarea cuando se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="d5af7-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="child-elements"></a><span data-ttu-id="d5af7-132">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d5af7-132">Child elements</span></span>



| <span data-ttu-id="d5af7-133">Elemento</span><span class="sxs-lookup"><span data-stu-id="d5af7-133">Element</span></span>                                                                                   | <span data-ttu-id="d5af7-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="d5af7-134">Type</span></span>     | <span data-ttu-id="d5af7-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5af7-135">Description</span></span>                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5af7-136">**Duration**</span><span class="sxs-lookup"><span data-stu-id="d5af7-136">**Duration**</span></span>](taskschedulerschema-duration-repetitiontype-element.md)                   | <span data-ttu-id="d5af7-137">duration</span><span class="sxs-lookup"><span data-stu-id="d5af7-137">duration</span></span> | <span data-ttu-id="d5af7-138">Especifica cuánto tiempo se repite el patrón.</span><span class="sxs-lookup"><span data-stu-id="d5af7-138">Specifies how long the pattern is repeated.</span></span><br/>                                                              |
| [<span data-ttu-id="d5af7-139">**Interval**</span><span class="sxs-lookup"><span data-stu-id="d5af7-139">**Interval**</span></span>](taskschedulerschema-interval-repetitiontype-element.md)                   | <span data-ttu-id="d5af7-140">duration</span><span class="sxs-lookup"><span data-stu-id="d5af7-140">duration</span></span> | <span data-ttu-id="d5af7-141">Especifica la cantidad de tiempo entre cada reinicio de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d5af7-141">Specifies the amount of time between each restart of the task.</span></span><br/>                                           |
| [<span data-ttu-id="d5af7-142">**StopAtDurationEnd**</span><span class="sxs-lookup"><span data-stu-id="d5af7-142">**StopAtDurationEnd**</span></span>](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | <span data-ttu-id="d5af7-143">boolean</span><span class="sxs-lookup"><span data-stu-id="d5af7-143">boolean</span></span>  | <span data-ttu-id="d5af7-144">Especifica que las instancias en ejecución de la tarea se detienen al final de la duración del patrón de repetición.</span><span class="sxs-lookup"><span data-stu-id="d5af7-144">Specifies that a running instances of the task is stopped at the end of the repetition pattern duration.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d5af7-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5af7-145">Remarks</span></span>

<span data-ttu-id="d5af7-146">Si especifica una duración de repetición para una tarea, también debe especificar el intervalo de repetición.</span><span class="sxs-lookup"><span data-stu-id="d5af7-146">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="d5af7-147">Si registra una tarea que contiene un desencadenador con un intervalo de repetición igual a un minuto y una duración de repetición igual a cuatro minutos, la tarea se iniciará cinco veces.</span><span class="sxs-lookup"><span data-stu-id="d5af7-147">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched five times.</span></span> <span data-ttu-id="d5af7-148">Las cinco repeticiones se pueden definir con el siguiente patrón.</span><span class="sxs-lookup"><span data-stu-id="d5af7-148">The five repetitions can be defined by the following pattern.</span></span>

1.  <span data-ttu-id="d5af7-149">Una tarea comienza al principio del primer minuto.</span><span class="sxs-lookup"><span data-stu-id="d5af7-149">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="d5af7-150">La siguiente tarea comienza al final del primer minuto.</span><span class="sxs-lookup"><span data-stu-id="d5af7-150">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="d5af7-151">La siguiente tarea comienza al final del segundo minuto.</span><span class="sxs-lookup"><span data-stu-id="d5af7-151">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="d5af7-152">La siguiente tarea comienza al final del tercer minuto.</span><span class="sxs-lookup"><span data-stu-id="d5af7-152">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="d5af7-153">La siguiente tarea comienza al final del cuarto minuto.</span><span class="sxs-lookup"><span data-stu-id="d5af7-153">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="d5af7-154">**Windows Server 2003, Windows XP y windows 2000:** Si registra una tarea que contiene un desencadenador con un intervalo de repetición igual a un minuto y una duración de repetición igual a cuatro minutos, la tarea se iniciará cuatro veces.</span><span class="sxs-lookup"><span data-stu-id="d5af7-154">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched four times.</span></span>

<span data-ttu-id="d5af7-155">**Windows Vista, Windows 7, Windows server 2008, Windows 8 y Windows server 2012:** Normalmente, el establecimiento de la duración de repetición en un múltiplo exacto del intervalo produce los números descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d5af7-155">**Windows Vista, Windows 7, Windows Server 2008, Windows 8 and Windows Server 2012:** Usually, setting the repetition duration to an exact multiple of the interval yields the numbers described above.</span></span> <span data-ttu-id="d5af7-156">Sin embargo, en ciertas condiciones de carga pesada, es posible que se agote el tiempo de espera antes de que TaskScheduler pueda iniciar el intervalo de tareas final.</span><span class="sxs-lookup"><span data-stu-id="d5af7-156">However, under certain heavy load conditions, it is possible for the duration to timeout before TaskScheduler can launch the final task interval.</span></span>

<span data-ttu-id="d5af7-157">Para el desarrollo de scripting, el patrón de repetición se especifica mediante la propiedad [**Trigger. repite**](trigger-repetition.md) heredada por todos los objetos de desencadenador.</span><span class="sxs-lookup"><span data-stu-id="d5af7-157">For scripting development, the repetition pattern is specified using the [**Trigger.Repetition**](trigger-repetition.md) property that is inherited by all the trigger objects.</span></span>

<span data-ttu-id="d5af7-158">En el desarrollo de C++, el patrón de repetición se especifica mediante la propiedad [**ITRigger:: repite**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) que heredan todas las interfaces del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="d5af7-158">For C++ development, the repetition pattern is specified using the [**ITRigger::Repetition**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) property that is inherited by all the trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="d5af7-159">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d5af7-159">Examples</span></span>

<span data-ttu-id="d5af7-160">En el código XML siguiente se define un elemento de desencadenador de arranque que especifica un patrón de repetición para un desencadenador.</span><span class="sxs-lookup"><span data-stu-id="d5af7-160">The following XML defines a boot trigger element that specifies a repetition pattern for a trigger.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition>
        <Interval></Interval>
        <Duration></Duration>
        <StopAtDurationEnd>true</StopAtDirationEnd>
    </Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="d5af7-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5af7-161">Requirements</span></span>



| <span data-ttu-id="d5af7-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5af7-162">Requirement</span></span> | <span data-ttu-id="d5af7-163">Value</span><span class="sxs-lookup"><span data-stu-id="d5af7-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d5af7-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5af7-164">Minimum supported client</span></span><br/> | <span data-ttu-id="d5af7-165">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d5af7-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d5af7-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5af7-166">Minimum supported server</span></span><br/> | <span data-ttu-id="d5af7-167">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5af7-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5af7-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5af7-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5af7-169">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="d5af7-169">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d5af7-170">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="d5af7-170">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





