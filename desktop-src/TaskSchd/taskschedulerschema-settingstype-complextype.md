---
title: Tipo complejo de settingsType
description: Define los elementos secundarios e información de secuenciación para el elemento de configuración (taskType).
ms.assetid: dba6b82d-aaa4-4f77-aeb1-c5a8f81aec25
keywords:
- tipo complejo de settingsType Programador de tareas
topic_type:
- apiref
api_name:
- settingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3c2b3128a35ee0e46c56d19badd431400d4d862
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686076"
---
# <a name="settingstype-complex-type"></a><span data-ttu-id="6a9af-104">Tipo complejo de settingsType</span><span class="sxs-lookup"><span data-stu-id="6a9af-104">settingsType Complex Type</span></span>

<span data-ttu-id="6a9af-105">Define los elementos secundarios e información de secuenciación para el elemento de [**configuración (taskType)**](taskschedulerschema-settings-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6a9af-105">Defines the child elements and sequencing information for the [**Settings (taskType)**](taskschedulerschema-settings-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="settingsType">
    <xs:all>
        <xs:element name="AllowStartOnDemand"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnFailure"
            type="restartType"
            minOccurs="0"
         />
        <xs:element name="MultipleInstancesPolicy"
            type="multipleInstancesPolicyType"
            default="IgnoreNew"
            minOccurs="0"
         />
        <xs:element name="DisallowStartIfOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StopIfGoingOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="AllowHardTerminate"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartWhenAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="NetworkProfileName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfNetworkAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="WakeToRun"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="Hidden"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DeleteExpiredTaskAfter"
            type="duration"
            default="PT0S"
            minOccurs="0"
         />
        <xs:element name="IdleSettings"
            type="idleSettingsType"
            minOccurs="0"
         />
        <xs:element name="NetworkSettings"
            type="networkSettingsType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
        <xs:element name="Priority"
            type="priorityType"
            default="7"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="UseUnifiedSchedulingEngine"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DisallowStartOnRemoteAppSession"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6a9af-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6a9af-106">Child elements</span></span>



| <span data-ttu-id="6a9af-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="6a9af-107">Element</span></span>                                                                                                             | <span data-ttu-id="6a9af-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a9af-108">Type</span></span>                                                                                              | <span data-ttu-id="6a9af-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a9af-109">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a9af-110">**AllowHardTerminate**</span><span class="sxs-lookup"><span data-stu-id="6a9af-110">**AllowHardTerminate**</span></span>](taskschedulerschema-allowhardterminate-settingstype-element.md)                           | <span data-ttu-id="6a9af-111">boolean</span><span class="sxs-lookup"><span data-stu-id="6a9af-111">boolean</span></span>                                                                                           | <span data-ttu-id="6a9af-112">Especifica si el servicio de Programador de tareas permite la finalización del hardware de la tarea.</span><span class="sxs-lookup"><span data-stu-id="6a9af-112">Specifies if the Task Scheduler service allows hard termination of the task.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="6a9af-113">**AllowStartOnDemand**</span><span class="sxs-lookup"><span data-stu-id="6a9af-113">**AllowStartOnDemand**</span></span>](taskschedulerschema-allowstartondemand-settingstype-element.md)                           | <span data-ttu-id="6a9af-114">boolean</span><span class="sxs-lookup"><span data-stu-id="6a9af-114">boolean</span></span>                                                                                           | <span data-ttu-id="6a9af-115">Especifica que la tarea se puede iniciar mediante el comando ejecutar o el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="6a9af-115">Specifies that the task can be started by using either the Run command or the Context menu.</span></span> <br/>                                                                                                                                                                                                             |
| [<span data-ttu-id="6a9af-116">**DeleteExpiredTaskAfter**</span><span class="sxs-lookup"><span data-stu-id="6a9af-116">**DeleteExpiredTaskAfter**</span></span>](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                   | <span data-ttu-id="6a9af-117">duration</span><span class="sxs-lookup"><span data-stu-id="6a9af-117">duration</span></span>                                                                                          | <span data-ttu-id="6a9af-118">Especifica la cantidad de tiempo que esperará el Programador de tareas antes de eliminar la tarea después de que expire.</span><span class="sxs-lookup"><span data-stu-id="6a9af-118">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="6a9af-119">Si no se especifica ningún valor para este elemento, el servicio Programador de tareas no eliminará la tarea.</span><span class="sxs-lookup"><span data-stu-id="6a9af-119">If no value is specified for this element, then the Task Scheduler service will not delete the task.</span></span><br/>                                                                                           |
| [<span data-ttu-id="6a9af-120">**DisallowStartIfOnBatteries**</span><span class="sxs-lookup"><span data-stu-id="6a9af-120">**DisallowStartIfOnBatteries**</span></span>](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)           | <span data-ttu-id="6a9af-121">boolean</span><span class="sxs-lookup"><span data-stu-id="6a9af-121">boolean</span></span>                                                                                           | <span data-ttu-id="6a9af-122">Especifica que la tarea no se iniciará si el equipo está funcionando con batería.</span><span class="sxs-lookup"><span data-stu-id="6a9af-122">Specifies that the task will not be started if the computer is running on battery power.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="6a9af-123">**DisallowStartOnRemoteAppSession**</span><span class="sxs-lookup"><span data-stu-id="6a9af-123">**DisallowStartOnRemoteAppSession**</span></span>](taskschedulerschema-disallowstartonremoteappsession-settingstype-element.md) | <span data-ttu-id="6a9af-124">boolean</span><span class="sxs-lookup"><span data-stu-id="6a9af-124">boolean</span></span>                                                                                           | <span data-ttu-id="6a9af-125">Especifica que la tarea no debe iniciarse si la tarea se desencadena para ejecutarse en una sesión de aplicaciones remotas integrada localmente (raíl).</span><span class="sxs-lookup"><span data-stu-id="6a9af-125">Specifies that the task should not start if the task is triggered to run in a Remote Applications Integrated Locally (RAIL) session.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="6a9af-126">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="6a9af-126">**Enabled**</span></span>](taskschedulerschema-enabled-settingstype-element.md)                                                 | <span data-ttu-id="6a9af-127">boolean</span><span class="sxs-lookup"><span data-stu-id="6a9af-127">boolean</span></span>                                                                                           | <span data-ttu-id="6a9af-128">Especifica que la tarea está habilitada.</span><span class="sxs-lookup"><span data-stu-id="6a9af-128">Specifies that the task is enabled.</span></span> <span data-ttu-id="6a9af-129">La tarea solo se puede realizar cuando este valor es **true**.</span><span class="sxs-lookup"><span data-stu-id="6a9af-129">The task can be performed only when this setting is **True**.</span></span><br/>                                                                                                                                                                                                        |
| [<span data-ttu-id="6a9af-130">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="6a9af-130">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-settingstype-element.md)                           | <span data-ttu-id="6a9af-131">duration</span><span class="sxs-lookup"><span data-stu-id="6a9af-131">duration</span></span>                                                                                          | <span data-ttu-id="6a9af-132">Especifica la cantidad de tiempo permitido para completar la tarea.</span><span class="sxs-lookup"><span data-stu-id="6a9af-132">Specifies the amount of time allowed to complete the task.</span></span><br/>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="6a9af-133">**Plusvalía**</span><span class="sxs-lookup"><span data-stu-id="6a9af-133">**Hidden**</span></span>](taskschedulerschema-hidden-settingstype-element.md)                                                   | <span data-ttu-id="6a9af-134">boolean</span><span class="sxs-lookup"><span data-stu-id="6a9af-134">boolean</span></span>                                                                                           | <span data-ttu-id="6a9af-135">Especifica, de forma predeterminada, que la tarea no estará visible en la interfaz de usuario (UI).</span><span class="sxs-lookup"><span data-stu-id="6a9af-135">Specifies, by default, that the task will not be visible in the user interface (UI).</span></span><br/>                                                                                                                                                                                                                     |
| [<span data-ttu-id="6a9af-136">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="6a9af-136">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md)                                       | [<span data-ttu-id="6a9af-137">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="6a9af-137">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)                      | <span data-ttu-id="6a9af-138">Especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="6a9af-138">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/>                                                                                                                                                                                                                   |
| [<span data-ttu-id="6a9af-139">**MultipleInstancesPolicy**</span><span class="sxs-lookup"><span data-stu-id="6a9af-139">**MultipleInstancesPolicy**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)                 | [<span data-ttu-id="6a9af-140">**multipleInstancesPolicyType**</span><span class="sxs-lookup"><span data-stu-id="6a9af-140">**multipleInstancesPolicyType**</span></span>](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | <span data-ttu-id="6a9af-141">Especifica la Directiva que define el modo en que el Programador de tareas se encarga de varias instancias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="6a9af-141">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span> <br/>                                                                                                                                                                                                     |
| [<span data-ttu-id="6a9af-142">**NetworkProfileName**</span><span class="sxs-lookup"><span data-stu-id="6a9af-142">**NetworkProfileName**</span></span>](taskschedulerschema-networkprofilename-settingstype-element.md)                           | <span data-ttu-id="6a9af-143">string</span><span class="sxs-lookup"><span data-stu-id="6a9af-143">string</span></span>                                                                                            | <span data-ttu-id="6a9af-144">Especifica el nombre de un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="6a9af-144">Specifies the name of a network profile.</span></span> <span data-ttu-id="6a9af-145">El servicio Programador de tareas comprueba la disponibilidad de esta red cuando el elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="6a9af-145">The Task Scheduler service verifies the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span> <span data-ttu-id="6a9af-146">El nombre se usa para fines de presentación.</span><span class="sxs-lookup"><span data-stu-id="6a9af-146">The name is used for display purposes.</span></span><br/>        |
| [<span data-ttu-id="6a9af-147">**NetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="6a9af-147">**NetworkSettings**</span></span>](taskschedulerschema-networksettings-settingstype-element.md)                                 | [<span data-ttu-id="6a9af-148">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="6a9af-148">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md)                | <span data-ttu-id="6a9af-149">Especifica la configuración que usa el servicio de Programador de tareas para obtener un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="6a9af-149">Specifies the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="6a9af-150">El servicio Programador de tareas comprueba la disponibilidad de esta red cuando el elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="6a9af-150">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |
| [<span data-ttu-id="6a9af-151">**Priority**</span><span class="sxs-lookup"><span data-stu-id="6a9af-151">**Priority**</span></span>](taskschedulerschema-priority-settingstype-element.md)                                               | [<span data-ttu-id="6a9af-152">**priorityType**</span><span class="sxs-lookup"><span data-stu-id="6a9af-152">**priorityType**</span></span>](taskschedulerschema-prioritytype-simpletype.md)                               | <span data-ttu-id="6a9af-153">Especifica el nivel de prioridad de la tarea.</span><span class="sxs-lookup"><span data-stu-id="6a9af-153">Specifies the priority level for the task.</span></span><br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="6a9af-154">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="6a9af-154">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md)                               | [<span data-ttu-id="6a9af-155">**restartType**</span><span class="sxs-lookup"><span data-stu-id="6a9af-155">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)                                | <span data-ttu-id="6a9af-156">Especifica que el Programador de tareas intentará reiniciar la tarea si se produce un error por algún motivo.</span><span class="sxs-lookup"><span data-stu-id="6a9af-156">Specifies that the Task Scheduler will attempt to restart the task if it fails for any reason.</span></span> <br/>                                                                                                                                                                                                          |
| [<span data-ttu-id="6a9af-157">**RunOnlyIfIdle**</span><span class="sxs-lookup"><span data-stu-id="6a9af-157">**RunOnlyIfIdle**</span></span>](taskschedulerschema-runonlyifidle-settingstype-element.md)                                     | <span data-ttu-id="6a9af-158">boolean</span><span class="sxs-lookup"><span data-stu-id="6a9af-158">boolean</span></span>                                                                                           | <span data-ttu-id="6a9af-159">Especifica que la tarea se ejecuta solo cuando el equipo está en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="6a9af-159">Specifies that the task is run only when the computer is in an idle state.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="6a9af-160">**RunOnlyIfNetworkAvailable**</span><span class="sxs-lookup"><span data-stu-id="6a9af-160">**RunOnlyIfNetworkAvailable**</span></span>](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)             | <span data-ttu-id="6a9af-161">boolean</span><span class="sxs-lookup"><span data-stu-id="6a9af-161">boolean</span></span>                                                                                           | <span data-ttu-id="6a9af-162">Especifica que el Programador de tareas ejecutará la tarea solo cuando una red esté disponible.</span><span class="sxs-lookup"><span data-stu-id="6a9af-162">Specifies that the Task Scheduler will run the task only when a network is available.</span></span><br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="6a9af-163">**StartWhenAvailable**</span><span class="sxs-lookup"><span data-stu-id="6a9af-163">**StartWhenAvailable**</span></span>](taskschedulerschema-startwhenavailable-settingstype-element.md)                           | <span data-ttu-id="6a9af-164">boolean</span><span class="sxs-lookup"><span data-stu-id="6a9af-164">boolean</span></span>                                                                                           | <span data-ttu-id="6a9af-165">Especifica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.</span><span class="sxs-lookup"><span data-stu-id="6a9af-165">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="6a9af-166">**StopIfGoingOnBatteries**</span><span class="sxs-lookup"><span data-stu-id="6a9af-166">**StopIfGoingOnBatteries**</span></span>](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md)                   | <span data-ttu-id="6a9af-167">boolean</span><span class="sxs-lookup"><span data-stu-id="6a9af-167">boolean</span></span>                                                                                           | <span data-ttu-id="6a9af-168">Especifica que la tarea se detendrá si el equipo cambia a la energía de la batería.</span><span class="sxs-lookup"><span data-stu-id="6a9af-168">Specifies that the task will be stopped if the computer switches to battery power.</span></span> <br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="6a9af-169">**UseUnifiedSchedulingEngine**</span><span class="sxs-lookup"><span data-stu-id="6a9af-169">**UseUnifiedSchedulingEngine**</span></span>](taskschedulerschema-useunifiedschedulingengine-settingstype-element.md)           | <span data-ttu-id="6a9af-170">boolean</span><span class="sxs-lookup"><span data-stu-id="6a9af-170">boolean</span></span>                                                                                           | <span data-ttu-id="6a9af-171">Especifica que la tarea se ejecuta mediante el motor de programación unificado.</span><span class="sxs-lookup"><span data-stu-id="6a9af-171">Specifies that the task is run by using the Unified Scheduling Engine.</span></span><br/>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="6a9af-172">**WakeToRun**</span><span class="sxs-lookup"><span data-stu-id="6a9af-172">**WakeToRun**</span></span>](taskschedulerschema-waketorun-settingstype-element.md)                                             | <span data-ttu-id="6a9af-173">boolean</span><span class="sxs-lookup"><span data-stu-id="6a9af-173">boolean</span></span>                                                                                           | <span data-ttu-id="6a9af-174">Especifica que Programador de tareas reactivará el equipo antes de ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="6a9af-174">Specifies that Task Scheduler will wake the computer before it runs the task.</span></span><br/>                                                                                                                                                                                                                            |



## <a name="requirements"></a><span data-ttu-id="6a9af-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a9af-175">Requirements</span></span>



| <span data-ttu-id="6a9af-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a9af-176">Requirement</span></span> | <span data-ttu-id="6a9af-177">Value</span><span class="sxs-lookup"><span data-stu-id="6a9af-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6a9af-178">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a9af-178">Minimum supported client</span></span><br/> | <span data-ttu-id="6a9af-179">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6a9af-179">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6a9af-180">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a9af-180">Minimum supported server</span></span><br/> | <span data-ttu-id="6a9af-181">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a9af-181">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a9af-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a9af-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a9af-183">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6a9af-183">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="6a9af-184">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6a9af-184">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





