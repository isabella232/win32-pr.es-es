---
title: Elemento Settings (taskType)
description: Especifica la configuración que el Programador de tareas utiliza para realizar la tarea.
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- Elemento Settings Programador de tareas
topic_type:
- apiref
api_name:
- Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9133d536aef692a5f9928e10963dff8c454f25fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422162"
---
# <a name="settings-tasktype-element"></a><span data-ttu-id="4283e-104">Elemento Settings (taskType)</span><span class="sxs-lookup"><span data-stu-id="4283e-104">Settings (taskType) Element</span></span>

<span data-ttu-id="4283e-105">Especifica la configuración que el Programador de tareas utiliza para realizar la tarea.</span><span class="sxs-lookup"><span data-stu-id="4283e-105">Specifies the settings that the Task Scheduler uses to perform the task.</span></span>

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="4283e-106">El elemento **Settings** se define mediante el tipo complejo [**taskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4283e-106">The **Settings** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4283e-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="4283e-107">Parent element</span></span>



| <span data-ttu-id="4283e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4283e-108">Element</span></span>                                          | <span data-ttu-id="4283e-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="4283e-109">Derived from</span></span>                                                 | <span data-ttu-id="4283e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4283e-110">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="4283e-111">**Task**</span><span class="sxs-lookup"><span data-stu-id="4283e-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="4283e-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="4283e-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="4283e-113">Especifica la tarea que realiza el servicio Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="4283e-113">Specifies the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="4283e-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4283e-114">Child elements</span></span>



| <span data-ttu-id="4283e-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="4283e-115">Element</span></span>                                                                                                          | <span data-ttu-id="4283e-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="4283e-116">Type</span></span>                                                                                              | <span data-ttu-id="4283e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4283e-117">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4283e-118">**AllowHardTerminate**</span><span class="sxs-lookup"><span data-stu-id="4283e-118">**AllowHardTerminate**</span></span>](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | <span data-ttu-id="4283e-119">boolean</span><span class="sxs-lookup"><span data-stu-id="4283e-119">boolean</span></span>                                                                                           | <span data-ttu-id="4283e-120">Especifica que la tarea puede terminar con TerminateProcess.</span><span class="sxs-lookup"><span data-stu-id="4283e-120">Specifies that the task may be terminated using TerminateProcess.</span></span><br/>                                         |
| [<span data-ttu-id="4283e-121">**AllowStartOnDemand**</span><span class="sxs-lookup"><span data-stu-id="4283e-121">**AllowStartOnDemand**</span></span>](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | <span data-ttu-id="4283e-122">boolean</span><span class="sxs-lookup"><span data-stu-id="4283e-122">boolean</span></span>                                                                                           | <span data-ttu-id="4283e-123">Especifica que la tarea se puede iniciar con el comando ejecutar o el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="4283e-123">Specifies that the task can be started using either the Run command or the Context menu.</span></span><br/>                  |
| [<span data-ttu-id="4283e-124">**DeleteExpiredTaskAfter**</span><span class="sxs-lookup"><span data-stu-id="4283e-124">**DeleteExpiredTaskAfter**</span></span>](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | <span data-ttu-id="4283e-125">duration</span><span class="sxs-lookup"><span data-stu-id="4283e-125">duration</span></span>                                                                                          | <span data-ttu-id="4283e-126">Especifica la cantidad de tiempo que esperará el Programador de tareas antes de eliminar la tarea después de que expire.</span><span class="sxs-lookup"><span data-stu-id="4283e-126">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span><br/> |
| [<span data-ttu-id="4283e-127">**DisallowStartIfOnBatteries**</span><span class="sxs-lookup"><span data-stu-id="4283e-127">**DisallowStartIfOnBatteries**</span></span>](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | <span data-ttu-id="4283e-128">boolean</span><span class="sxs-lookup"><span data-stu-id="4283e-128">boolean</span></span>                                                                                           | <span data-ttu-id="4283e-129">Especifica que la tarea no se iniciará si el equipo se está ejecutando con baterías.</span><span class="sxs-lookup"><span data-stu-id="4283e-129">Specifies that the task will not be started if the computer is running on batteries.</span></span><br/>                      |
| [<span data-ttu-id="4283e-130">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="4283e-130">**Enabled**</span></span>](taskschedulerschema-enabled-settingstype-element.md)                                              | <span data-ttu-id="4283e-131">boolean</span><span class="sxs-lookup"><span data-stu-id="4283e-131">boolean</span></span>                                                                                           | <span data-ttu-id="4283e-132">Especifica que la tarea está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4283e-132">Specifies that the task is enabled.</span></span> <span data-ttu-id="4283e-133">La tarea solo se puede realizar cuando este valor es true.</span><span class="sxs-lookup"><span data-stu-id="4283e-133">The task can be performed only when this setting is True.</span></span><br/>             |
| [<span data-ttu-id="4283e-134">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="4283e-134">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | <span data-ttu-id="4283e-135">duration</span><span class="sxs-lookup"><span data-stu-id="4283e-135">duration</span></span>                                                                                          | <span data-ttu-id="4283e-136">Cantidad de tiempo permitido para completar la tarea.</span><span class="sxs-lookup"><span data-stu-id="4283e-136">Amount of time allowed to complete the task.</span></span><br/>                                                              |
| [<span data-ttu-id="4283e-137">**Plusvalía**</span><span class="sxs-lookup"><span data-stu-id="4283e-137">**Hidden**</span></span>](taskschedulerschema-hidden-settingstype-element.md)                                                | <span data-ttu-id="4283e-138">boolean</span><span class="sxs-lookup"><span data-stu-id="4283e-138">boolean</span></span>                                                                                           | <span data-ttu-id="4283e-139">Especifica que la tarea no será visible de forma predeterminada en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4283e-139">Specifies that the task will not be visible in the UI by default.</span></span><br/>                                         |
| [<span data-ttu-id="4283e-140">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="4283e-140">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [<span data-ttu-id="4283e-141">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="4283e-141">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)                      | <span data-ttu-id="4283e-142">Especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="4283e-142">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/>                    |
| [<span data-ttu-id="4283e-143">**MaintenanceSettings**</span><span class="sxs-lookup"><span data-stu-id="4283e-143">**MaintenanceSettings**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [<span data-ttu-id="4283e-144">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="4283e-144">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md)        | <span data-ttu-id="4283e-145">Especifica cómo realiza el Programador de tareas las tareas durante el mantenimiento automático.</span><span class="sxs-lookup"><span data-stu-id="4283e-145">Specifies how the Task Scheduler performs tasks during Automatic maintenance.</span></span><br/>                             |
| [<span data-ttu-id="4283e-146">**MultipleInstancesPolicy**</span><span class="sxs-lookup"><span data-stu-id="4283e-146">**MultipleInstancesPolicy**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [<span data-ttu-id="4283e-147">**multipleInstancesPolicyType**</span><span class="sxs-lookup"><span data-stu-id="4283e-147">**multipleInstancesPolicyType**</span></span>](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | <span data-ttu-id="4283e-148">Especifica la Directiva que define el modo en que el Programador de tareas se encarga de varias instancias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="4283e-148">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span><br/>       |
| [<span data-ttu-id="4283e-149">**Priority**</span><span class="sxs-lookup"><span data-stu-id="4283e-149">**Priority**</span></span>](taskschedulerschema-priority-settingstype-element.md)                                            | [<span data-ttu-id="4283e-150">**priorityType**</span><span class="sxs-lookup"><span data-stu-id="4283e-150">**priorityType**</span></span>](taskschedulerschema-prioritytype-simpletype.md)                               | <span data-ttu-id="4283e-151">Especifica el nivel de prioridad de la tarea.</span><span class="sxs-lookup"><span data-stu-id="4283e-151">Specifies the priority level for the task.</span></span><br/>                                                                |
| [<span data-ttu-id="4283e-152">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="4283e-152">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [<span data-ttu-id="4283e-153">**restartType**</span><span class="sxs-lookup"><span data-stu-id="4283e-153">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)                                | <span data-ttu-id="4283e-154">Especifica que el Programador de tareas intentará reiniciar la tarea si se produce un error en la tarea por cualquier motivo.</span><span class="sxs-lookup"><span data-stu-id="4283e-154">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/>      |
| [<span data-ttu-id="4283e-155">**RunOnlyIfIdle**</span><span class="sxs-lookup"><span data-stu-id="4283e-155">**RunOnlyIfIdle**</span></span>](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | <span data-ttu-id="4283e-156">boolean</span><span class="sxs-lookup"><span data-stu-id="4283e-156">boolean</span></span>                                                                                           | <span data-ttu-id="4283e-157">Especifica que la tarea se ejecuta solo cuando el equipo está en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="4283e-157">Specifies that the task is run only when the computer is in an idle state.</span></span><br/>                                |
| [<span data-ttu-id="4283e-158">**RunOnlyIfNetworkAvailable**</span><span class="sxs-lookup"><span data-stu-id="4283e-158">**RunOnlyIfNetworkAvailable**</span></span>](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | <span data-ttu-id="4283e-159">boolean</span><span class="sxs-lookup"><span data-stu-id="4283e-159">boolean</span></span>                                                                                           | <span data-ttu-id="4283e-160">Especifica que el Programador de tareas ejecutará la tarea solo cuando una red esté disponible.</span><span class="sxs-lookup"><span data-stu-id="4283e-160">Specifies that the Task Scheduler will run the task only when a network is available.</span></span><br/>                     |
| [<span data-ttu-id="4283e-161">**StartWhenAvailable**</span><span class="sxs-lookup"><span data-stu-id="4283e-161">**StartWhenAvailable**</span></span>](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | <span data-ttu-id="4283e-162">boolean</span><span class="sxs-lookup"><span data-stu-id="4283e-162">boolean</span></span>                                                                                           | <span data-ttu-id="4283e-163">Especifica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.</span><span class="sxs-lookup"><span data-stu-id="4283e-163">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span><br/>     |
| [<span data-ttu-id="4283e-164">**StopIfGoingOnBatteries (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="4283e-164">**StopIfGoingOnBatteries (settingsType)**</span></span>](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | <span data-ttu-id="4283e-165">boolean</span><span class="sxs-lookup"><span data-stu-id="4283e-165">boolean</span></span>                                                                                           | <span data-ttu-id="4283e-166">Especifica que la tarea se detendrá si el equipo pasa a baterías.</span><span class="sxs-lookup"><span data-stu-id="4283e-166">Specifies that the task will be stopped if the computer is going onto batteries.</span></span><br/>                          |
| [<span data-ttu-id="4283e-167">**Volatil**</span><span class="sxs-lookup"><span data-stu-id="4283e-167">**Volatile**</span></span>](taskschedulerschema-volatile-element.md)                                                         | <span data-ttu-id="4283e-168">boolean</span><span class="sxs-lookup"><span data-stu-id="4283e-168">boolean</span></span>                                                                                           | <span data-ttu-id="4283e-169">Especifica si la tarea se deshabilitará automáticamente mediante Programador de tareas en el inicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="4283e-169">Specifies if the task is automatically disabled by Task Scheduler at Windows startup.</span></span><br/>                     |
| [<span data-ttu-id="4283e-170">**WakeToRun (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="4283e-170">**WakeToRun (settingsType)**</span></span>](taskschedulerschema-waketorun-settingstype-element.md)                           | <span data-ttu-id="4283e-171">boolean</span><span class="sxs-lookup"><span data-stu-id="4283e-171">boolean</span></span>                                                                                           | <span data-ttu-id="4283e-172">Especifica que Programador de tareas reactivará el equipo cuando sea el momento de ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="4283e-172">Specifies that Task Scheduler will wake the computer when it is time to run the task.</span></span><br/>                     |



## <a name="remarks"></a><span data-ttu-id="4283e-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4283e-173">Remarks</span></span>

<span data-ttu-id="4283e-174">Puede seleccionar uno o varios de los elementos secundarios a los que se hace referencia anteriormente.</span><span class="sxs-lookup"><span data-stu-id="4283e-174">You can select one or more of the child elements referenced above.</span></span>

<span data-ttu-id="4283e-175">En el desarrollo de C++, la información de registro de una tarea se especifica mediante la [**propiedad settings de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).</span><span class="sxs-lookup"><span data-stu-id="4283e-175">For C++ development, the registration information of a task is specified using the [**Settings property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).</span></span>

<span data-ttu-id="4283e-176">Para el desarrollo de scripting, la información de registro de una tarea se especifica mediante la propiedad [**TaskDefinition. Settings**](taskdefinition-settings.md) .</span><span class="sxs-lookup"><span data-stu-id="4283e-176">For scripting development, the registration information of a task is specified using the [**TaskDefinition.Settings**](taskdefinition-settings.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="4283e-177">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4283e-177">Examples</span></span>

<span data-ttu-id="4283e-178">En el siguiente ejemplo de código XML se define un elemento de configuración que permite una finalización rígida de la tarea.</span><span class="sxs-lookup"><span data-stu-id="4283e-178">The following XML code example defines a settings element that allows a hard termination of the task.</span></span>


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



<span data-ttu-id="4283e-179">Para obtener más información y un ejemplo completo del XML para establecer la configuración de la tarea, vea [ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="4283e-179">For more information and a complete example of the XML for setting task settings, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4283e-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4283e-180">Requirements</span></span>



| <span data-ttu-id="4283e-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="4283e-181">Requirement</span></span> | <span data-ttu-id="4283e-182">Value</span><span class="sxs-lookup"><span data-stu-id="4283e-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4283e-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4283e-183">Minimum supported client</span></span><br/> | <span data-ttu-id="4283e-184">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4283e-184">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4283e-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4283e-185">Minimum supported server</span></span><br/> | <span data-ttu-id="4283e-186">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4283e-186">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4283e-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="4283e-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4283e-188">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="4283e-188">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="4283e-189">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="4283e-189">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





